+++
title = "Add template"
description = "This section describes how to add a template"
weight = 6
+++

This section describes how to add a website template

### 1. Navigate to the according directory and add template file

{{< code lang="bash" >}}
path: website_generator/public/templates/<TEMPLATE FOLDER NAME> 
{{< /code >}} 

### 2. Change .html files to .ejs
This is to ensure that we can pass in data and then regerate the page. 
Read more on EJS: https://ejs.co/

### 3. Ex : Passing in data and populating 

This is an example of data that would passed in the .ejs file
{{< code lang="js" >}}
{
  firstName: 'Akilan',
  lastName: 'Selvacoumar',
  companyName: 'Test123',
  logoUrl: 'https://hwtech.club/images/output-onlinepngtools.png',
  bannerUrl: 'https://i.ytimg.com/vi/SIQHKaMOCbU/maxresdefault.jpg',
  email: 'akilanselva@hotmail.com',
  description: 'Loldfsdf sdfsdsdsfsd sd fsdrs d sdf ',
  template: 'Colo_Shop',
  csv: [
    {
      'product id': '1',
      'product name': 'java',
      description: "We all love java fsdf sdf' sd'f 'sdf sfsdf sdf sdf",
      cost: '130',
      'product image url': 'https://i.stack.imgur.com/WxVXe.jpg'
    },
    {
      'product id': '2',
      'product name': 'C',
      description: 'C lord it is',
      cost: '200',
      'product image url': 'https://images-na.ssl-images-amazon.com/images/I/41IlAcQj9nL.jpg'
    }
  ],
  id: 'Test123_50'
}

{{< /code >}} 

#### Ex: .ejs file layout

{{< code lang="java" >}}


<body>
...

		<!-- Slider -->

		<div class="main_slider"
			style="background-image:url('<%= bannerUrl %>')">
			<div class="container fill_height">
				<div class="row align-items-center fill_height">

				</div>
			</div>
		</div>

		<!-- New Arrivals -->

		<div class="new_arrivals">
			<div class="container">
				<div class="row">
					<div class="col text-center">
						<div class="section_title new_arrivals_title">
							<h2>Our Products</h2>
							<p><%= description %></p>
						</div>
					</div>
				</div>
				...
				<div class="row">
					<div class="col">
						<div class="product-grid"
							data-isotope='{ "itemSelector": ".product-item", "layoutMode": "fitRows" }'>

							<!-- Product 3 -->
                        <% for(var i = 0; i < csv.length ; i++) {%>
							<div class="product-item *">
								<div class="product product_filter">
									<div class="product_image">
										<img src="<%= csv[i]['product image url'] %>" alt="">
									</div>
									<div class="product_info">
										<h6 class="product_name"><a href="#"><a><%= csv[i]["product name"] %></a></h6>
										<p><%= csv[i]["description"] %></p>
										<div class="product_price">$<%= csv[i].cost %></div>
									</div>
									<br>
									<div class="cart"><div class="red_button add_to_cart_button"><a onClick="additem('<%= csv[i]['product name'] %>', <%= csv[i].cost %>)" style="color:white">Add to cart</a></div></div>
								</div>
							</div>
						<% } %>
...
</body>

</html>

{{< /code >}}