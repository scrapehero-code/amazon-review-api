# Amazon Review API using Flask & Selectorlib

A very basic API to scrape product reviews from Amazon and get data in real time as JSON with all fields, that amazon product adverstising api does not provide you. 

Full Tutorail - [Amazon Product Reviews API – build you own using Python](https://www.scrapehero.com/free-amazon-product-reviews-api-build-you-own-using-python/)

## Usage

Go into the project folder 

1. Install requirements `pip install -r requirements.txt`
2. Set FLASK_APP - `export FLASK_APP=app.py`
3. Run App - `flask run`
4. Call API with Review Page URL. Eg: `http://localhost:5000/?url=https://www.amazon.com/Nike-Womens-Reax-Running-Shoes/product-reviews/B07ZPL752N/ref=cm_cr_dp_d_show_all_btm?ie=UTF8&reviewerType=all_reviews`

## Example Data Format

```json
{
  "product_title": "Nike Women's Reax Run 5 Running Shoes", 
  "number_of_reviews": "794  customer ratings", 
  "average_rating": 4.4, 
  "histogram": {
    "1 star": "5%", 
    "2 star": "4%", 
    "3 star": "6%", 
    "4 star": "11%", 
    "5 star": "73%"
  }, 
  "next_page": "https://www.amazon.com/Nike-Womens-Reax-Running-Shoes/product-reviews/B07ZPL752N/ref=cm_cr_arp_d_paging_btm_2?ie=UTF8&pageNumber=2", 
  "reviews": [
    {
      "author": "Diane Johnson", 
      "content": "I love the shoes they are true to size , I wear a 7 1/2 but I ordered a 8 to allow a little extra room and I got just that", 
      "date": "18 Sep 2018", 
      "found_helpful": "92 people found this helpful", 
      "images": "https://images-na.ssl-images-amazon.com/images/I/81wdRdaAfmL._SY88.jpg", 
      "product": "Nike Women's Reax Run 5 Running Shoes", 
      "rating": "5.0", 
      "title": "Look just like the photo", 
      "url": "https://www.amazon.com/Nike-Womens-Reax-Running-Shoes/product-reviews/B07ZPL752N/ref=cm_cr_dp_d_show_all_btm?ie=UTF8", 
      "variant": "Size: 8 Color: White/Metallic Silver/Dark Grey", 
      "verified_purchase": true
    }, 
    {
      "author": "sherlain miranda", 
      "content": "Just writing a rare review on these . I love Nike\u2019s but my feet don\u2019t usually. So I\u2019ve ordered and returned a lot. Tried again lol and these ARE AMAZING comfortable. So much that I may order 3 more this year just to have them. The color is so cute and clean and sporty. I\u2019m 99.9% sure I\u2019ve dinally found a pair of Nikes I\u2019m not going to return , fingers crossed \ud83e\udd1e\ud83d\ude0a", 
      "date": "08 May 2019", 
      "found_helpful": "63 people found this helpful", 
      "images": "https://images-na.ssl-images-amazon.com/images/I/717EKthL0BL._SY88.jpg", 
      "product": "Nike Women's Reax Run 5 Running Shoes", 
      "rating": "4.0", 
      "title": "After 20 returns", 
      "url": "https://www.amazon.com/Nike-Womens-Reax-Running-Shoes/product-reviews/B07ZPL752N/ref=cm_cr_dp_d_show_all_btm?ie=UTF8", 
      "variant": "Size: 10 Color: White/Metallic Silver/Dark Grey", 
      "verified_purchase": true
    }
  ]
}
```
# Disclaimer

This was not built for production deployments. You may want to check [Flask Deployment Guidelines](https://flask.palletsprojects.com/en/1.1.x/deploying/#deployment)

Any code provided in our tutorials is for illustration and learning purposes only. We are not responsible for how it is used and assume no liability for any detrimental usage of the source code. The mere presence of this code on our repository does not imply that we encourage scraping or scrape the websites referenced in the code and accompanying tutorial. The tutorials only help illustrate the technique of programming web scrapers for popular internet websites. We are not obligated to provide any support for the code, however, if you add your questions in the comments section, we may periodically address them.
