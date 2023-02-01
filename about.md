---
layout: page
image: /assets/img/blog/hydejack-9.jpg
description: >
    Hi, I am Sandy,I am Salvadoran, I can help you to have the best experience in El Salvador, the country of surf, bitcoin and liberty.
hide_description: true

---

About me.

I am a Salvadoran, and I can help you have a great experience exploring El Salvador together.
If you want to know more do not hesitate to follow our social networks and contact us.

![Volcano](/assets/img/about/about-me.jpg)

Discover the Beauty of El Salvador with a Professional Tour Guide
Planning a trip to El Salvador and looking for an immersive and personalized experience? Look no further! As a licensed and experienced tour guide, I am here to provide you with top-notch tour services that will make your visit unforgettable.


Don't miss your chance to get the most out of your visit to El Salvador. Book your tour with me today and let me show you why this place is so special.
For more information, please get in contact with us. I look forward to hearing from you and guiding you on the adventure of a lifetime!
---
<script>
  window.onload = function() {
    const accessToken = '861a85e75788675384fc9fd0bae83255';
    const instagramUsername = 'YOUR_INSTAGRAM_USERNAME';
    const apiEndpoint = `https://api.instagram.com/v1/users/${instagramUsername}/media/recent/?access_token=${accessToken}`;

    fetch(apiEndpoint)
      .then(response => response.json())
      .then(data => {
        const posts = data.data;
        posts.forEach(post => {
          const imgSrc = post.images.standard_resolution.url;
          const postLink = post.link;

          const instagramPost = document.createElement('a');
          instagramPost.setAttribute('href', postLink);
          instagramPost.setAttribute('target', '_blank');

          const instagramImage = document.createElement('img');
          instagramImage.setAttribute('src', imgSrc);

          instagramPost.appendChild(instagramImage);

          document.getElementById('instagram-feed').appendChild(instagramPost);
        });
      });
  };
</script>

<div id="instagram-feed"></div>

{% include contact-form.html %}
