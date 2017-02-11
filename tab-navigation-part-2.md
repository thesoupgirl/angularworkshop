# Tab Navigation Part 2

Now we have only the home tab working, so if you click another tab, nothing actually happens...Now that's awkward.  Let's try to get the About Me tab up and working.  Before we can do that, we need some content for our About Me page.  Here's some sample content that I came up with:

```
<div style="margin-top: 20px; margin-bottom: 25px;">
    <section id="aboutme" class="aboutme">
    <div class="container">
        <div class="row style="margin-top: 80px; margin-bottom: 25px;">
            <div class="sec-title text-center wow fadeInUp animated" data-wow-duration="700ms">
                <h2>Meet Me</h2>
                <div class="devider"><i class="fa fa-lg"></i></div>
            </div>
            
            <div class="sec-sub-title text-center wow fadeInRight animated" data-wow-duration="500ms">
                <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque </p>
            </div>
            
            <!-- me -->
            <figure class="team-member col-md-3 col-sm-6 col-xs-12 text-center wow fadeInUp animated" data-wow-duration="500ms">
                <div class="member-thumb">
                    <img src="puppy.jpg" alt="Me" class="img-responsive">
                    <figcaption class="overlay">
                        <h5>Text here</h5>
                        <p> More text here </p>
                        <ul class="social-links text-center">
                            <li><a href="https://twitter.com/yourtwitter"><i class="fa fa-twitter fa-lg></i></a></li>
                            <li><a href="https://facebook.com/yourfb"><i class="fa fa-facebook fa-lg></i></a></li>
                            <li><a href="https://google.com/yourgoogleplus"><i class="fa fa-google-plus fa-lg></i></a></li>
                        </ul>
                    </figcaption>
                </div>
                
                <h4>FirstName LastName</h4>
                <span>CS Student</span>
            </figure>
        </div>
        </div>
        </section>
        </div>
```



