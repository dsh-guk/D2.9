<p>u1 = User.objects.create_user(username='Anohina')</p>
<p>u2 = User.objects.create_user(username='Popov')</p>
<p>Author.objects.create(authorUser=u1)</p>
<p>Author.objects.create(authorUser=u2)</p>
<p>Category.objects.create(name='IT')</p>
<p>Category.objects.create(name='fantastic')</p>
<p>Category.objects.create(name='scifi')</p>
<p>Category.objects.create(name='poetry')</p>
<p>author = Author.objects.get(id=1)</p>
<p>Post.objects.create(author=author,&nbsp;categoryType='NW', head='Monday's weather', text='Monday's weather'</p>
<p>Post.objects.create(author=author,&nbsp;categoryType='AR', head='Sweet and sour drink in cold weather', text='Peel and peel the lemon, orange and grapefruit slices. Put the karkade and fruit in a saucepan. Pre-boil the water, pour it over the fruit and tea.'</p>
<p>Post.objects.create(author=author,&nbsp;categoryType='AR', head='Fragrant sea buckthorn tea', text='mash the sea buckthorn with a fork, add ginger, mix. Add sugar and mix the mass again. Fill with water and put on fire. When the tea boils, remove from the heat, put the spices in a saucepan and cover with a lid. Tea is infused for at least 7 minutes. Honey is added before serving.'</p>
