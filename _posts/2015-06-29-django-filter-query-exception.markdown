---
layout: post
title: "Django Filter Query Exception"
date: 2015-06-29 11:44:20
tags: "django django-exception django-filter-query"
---

While looking for answers on this question: "Does multiple monitor increase
programmer's productivity?", I found interesting tips from
[Joelon Software](http://www.joelonsoftware.com/articles/fog0000000043.html)
blog post. It's the fourth Joel's Test: **A Bug Database**. 

Since, I still don't know yet what tool will help us to store our bugs, I'll
write my _first_ bug in this blog post. And also I'd like to know how to write
snippet in Jekyll, which powered this blog. 

So, let's give it a shot! 

Example, I am querying database using Django query filter. 

{% highlight python %}

	try:
		borrowed_books = Book.objects.filter(borrow_date__lte=datetime.today(),
							user=request.user, borrow_status=True)
	except Book.DoesNotExist:
		raise Http404("You're not borrowing any books")

{% endhighlight %}

This code will not return the exception eventhough there is no match with the
filter rule. **No match filter query will only return empty list**. So, I need to
fix the code. 

Let's try to debug using the django shell.

{% highlight python %}

>>> from aurora.apps.users.models import User
>>> u1 = User.objects.get(email='borrower101@aurora.co')
>>> from aurora.apps.books.models import Book
>>> borrowing = Book.objects.filter(borrow_date__lte=datetime.today(), user=u,
				borrow_status=True)
[]
>>> u2 = User.objects.get(email='borrower102@aurora.co')
>>> borrowing = Book.objects.filter(borrow_date__lte=datetime.today(), user=u,
				borrow_status=True)
[<Book: Dahl, Roald>, <Book: Griffith, Andy>]

{% endhighlight %}

So user u1 doesn't borrow any books while u2 borrows 2 books. What to do to
improve this code? We could check the query length. If the query length equalas
to zero then we could throw the exception. 

{% highlight python %}

	borrowed_books = Book.objects.filter(borrow_date__lte=datetime.today(),
						user=request.user, borrow_status=True)
	if borrowed_books.count() == 0:		
		raise Http404("You're not borrowing any books")

{% endhighlight %}

That's all for now. 

