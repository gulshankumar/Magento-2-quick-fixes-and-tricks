# Magento-2-quick-fixes-and-tricks

# Scroll to top after add to cart
### put below code insize script tag in any .phtml that renders on catalog page
`require(['jquery'],function($){
                $(document).on('ajax:addToCart', function (event) {
                    setTimeout(function(){
                        $('html, body').animate({scrollTop:0}, 'slow');
                    }, 1000);
                });
            });`
