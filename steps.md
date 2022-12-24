<p>u1 = User.objects.create_user(username='Anohina')</p>
<p>u2 = User.objects.create_user(username='Popov')</p>

<p>Author.objects.create(authorUser=u1)</p>
<p>Author.objects.create(authorUser=u2)</p>

<p>Category.objects.create(name='IT')</p>
<p>Category.objects.create(name='fantastic')</p>
<p>Category.objects.create(name='scifi')</p>
<p>Category.objects.create(name='poetry')</p>

<p>author = Author.objects.get(id=1)</p>
<p>Post.objects.create(author=author,&nbsp;categoryType='NW', head='weather', text='weather')</p>
<p>Post.objects.create(author=Author.objects.get(id=2), categoryType='AR', head='Article1', text='textArticle1')</p>
<p>Post.objects.create(author=Author.objects.get(id=2), categoryType='AR', head='Article2', text='textArticle2')</p>

<p>Post.objects.get(id=1).postCategory.add(Category.objects.get(id=1))</p> #добавление категории в пост
<p>Post.objects.get(id=1).postCategory.add(Category.objects.get(id=2))</p>
<p>Post.objects.get(id=2).postCategory.add(Category.objects.get(id=3))</p>
<p>Post.objects.get(id=3).postCategory.add(Category.objects.get(id=4))</p>

<p>Comment.objects.create(commentPost=Post.objects.get(id=1), commentUser=Author.objects.get(id=1).authorUser, text='firstcomment')</p> 
<p>Comment.objects.create(commentPost=Post.objects.get(id=2), commentUser=Author.objects.get(id=2).authorUser, text='secondcomment')</p>
<p>Comment.objects.create(commentPost=Post.objects.get(id=3), commentUser=Author.objects.get(id=2).authorUser, text='thirdcomment')</p>

<p>Comment.objects.get(id=1).dislike()</p>
<p>Comment.objects.get(id=2).like()</p> 
<p>Comment.objects.get(id=3).like()</p> 
<p>Comment.objects.get(id=2).like()</p>

<p>Author.objects.get(id=1)</p>
<p>a = Author.objects.get(id=1)</p>
<p>a.update_rating()</p>
<p>a.ratingAuthor</p>

<p>Author.objects.get(id=2)</p>
<p>b = Author.objects.get(id=2)</p>
<p>b.update_rating()</p>
<p>b.ratingAuthor</p>

<p>a = Author.objects.order_by('-ratingAuthor')</p>  #<QuerySet [<Author: Author object (2)>, <Author: Author object (1)>]>


