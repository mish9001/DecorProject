<html>
<head>
    <meta name="viewport" content="width=device-width" />
    <title>Index</title>
</head>
<body>

    <h3>Products List</h3>
    
    <table class="table">
  
    <tr>
        <th>Id</th>
        <th>Name</th>
        <th>Photo</th>
        <th>Price</th>
        <th>Buy</th>
    </tr>
    @foreach (Product product in ViewBag.products)
    {
        <tr>
            <td>@product.Id</td>
            <td>@product.Name</td>
            <td><img src="~/Content/Images/@product.Photo" width="300" /> </td>
            <td>@product.Price</td>
            <td align="center">
                <a href="@Url.Action("Buy", "Cart", new { id = product.Id })">Add To Cart</a>
            </td>
        </tr>
    }
</table>



</body>
</html>
