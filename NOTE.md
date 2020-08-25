## Part 1 - Setup and Project Config
- Download the boilerplate.
- Create the virtual environment and activate it.
- Install the pip dependencies.
- Configure allauth from [here](https://django-allauth.readthedocs.io/en/latest/installation.html)
- Test with /accounts/login
- Create models at a primary level
- Create item_list view, configure urls.py, and create item_list.html
- Download ecommerce template from [here](https://mdbootstrap.com/freebies/jquery/e-commerce/)
- Move the template static files to static_files directory
- Move the template html files to tempaltes directory
- Add the static reference in necessary links in the base home-page.html

## Part 2 - Adding Items to a Cart
- Edit the model: Item
- Create category and label choices where in each tuple the first element is saved in db, and the other one is displayed.
- In DetailView url, <pk> or <slug> must be included as every page will display an individual item.
- Implement item model and add_to_cart and remove_from_cart functionalities.
- Implement django flash messages with MDB alerts in the base.html. {{ message.tags }} denotes default, info, primary, secondary, danger, etc. bootstrap color tags.

## Part 3 - Improving the UI
- Customize the home.html, footer.html, navbar.html
- Download and integrate allauth template from [here](https://github.com/pennersr/django-allauth/tree/master/allauth/templates)
- Install and configure crispy forms in settings.py.
- In settings.py add the following line to direct to this path after successful login. LOGIN_REDIRECT_URL = '/'
- Include paginate_by = int to initiate pagination in HomeView(ListView).
- Edit the pagination section in home.html
- Add core/templatetags/cart_template_tags.py for showing cart count.
- Load cart_template_tags in the navbar.html. In the place of cart count add {{ request.user|cart_item_count }}. Here 'cart_item_count' is the function name and 'request.user' is the argument passed like cart_item_count(request.user)
