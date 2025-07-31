<section data-bs-version="5.1" class="header18" group="Headers" data-bg-video="{{bg.type == 'video' && bg.value.url}}" mbr-class="{'mbr-fullscreen': fullScreen, 'mbr-parallax-background': bg.parallax}">
  <mbr-parameters>
    <header>Size</header>
    <input type="checkbox" title="Full Screen" name="fullScreen" checked>
    <input type="checkbox" title="Full Width" name="fullWidth" checked>
    <input type="range" inline title="Top" name="paddingTop" min="0" max="24" step="1" value="20" condition="fullScreen == false">
    <input type="range" inline title="Bottom" name="paddingBottom" min="0" max="12" step="1" value="4" condition="fullScreen == false">
    <input type="range" inline title="Content Width" name="contentWidth" min="3" max="12" step="1" value="12">
    <header>Show / Hide</header>
    <input type="checkbox" title="Title" name="showTitle" checked>
    <input type="checkbox" title="Subtitle" name="showSubtitle">
    <input type="checkbox" title="Text" name="showText" checked>
    <input type="checkbox" title="Buttons" name="showButtons" checked>
    <select title="Vertical Align" name="verticalAlign" condition="fullScreen">
      <option value="flex-start">Top</option>
      <option value="center">Center</option>
      <option value="flex-end" selected>Bottom</option>
    </select>
    <select title="Horizontal Align" name="horizontalAlign">
      <option value="flex-start" selected>Left</option>
      <option value="center">Center</option>
      <option value="flex-end">Right</option>
    </select>
    <header>Background</header>
    <fieldset type="background" name="bg" parallax>
      <input type="image" title="Image" value="../_images/background17.jpg" parallax>
      <input type="video" title="Video" value="https://www.youtube.com/embed/ZOZOqbK86t0?autoplay=1&loop=1&playlist=ZOZOqbK86t0&t=20&mute=1&playsinline=1&controls=0&showinfo=0&autohide=1&allowfullscreen=true&mode=transparent" selected>
      <input type="color" title="Color" value="#260a30">
    </fieldset>
    <header condition="bg.type === 'video'">Fallback Image</header>
    <input type="image" title="Fallback Image" value="../_images/background1.jpg" name="fallBackImage" condition="bg.type === 'video'">
    <input type="checkbox" title="Overlay" name="overlay" condition="bg.type !== 'color'">
    <input type="color" title="Overlay Color" name="overlayColor" value="#ffffff" condition="overlay && bg.type !== 'color'">
    <input type="range" inline title="Opacity" name="overlayOpacity" min="0" max="1" step="0.1" value="0.8" condition="overlay && bg.type !== 'color'">

    <input type="checkbox" title="Overlay" name="overlay" condition="bg.type!='color'" checked>
    <input type="color" title="Overlay Color" name="overlayColor" value="#000000" condition="bg.type!='color' && overlay">
    <input type="range" inline title="Overlay Opacity" name="overlayOpacity" min="0" max="1" step="0.1" value="0.5" condition="bg.type!='color' && overlay">
  </mbr-parameters>

  <div class="mbr-overlay" mbr-if="overlay && bg.type !== 'color'" opacity="{{overlayOpacity}}" bg-color="{{overlayColor}}"></div>
  <div mbr-class="{'container': !fullWidth, 'container-fluid': fullWidth}">
    <div class="row">
      <div class="content-wrap col-12 col-md-{{contentWidth}}">
        <h1 class="mbr-section-title mbr-fonts-style mbr-white mb-4" mbr-theme-style="display-1" data-app-selector=".mbr-section-title" mbr-if="showTitle">
          <b>EIE Auto</b>
        </h1>
        <h2 class="mbr-section-subtitle mbr-fonts-style mbr-white mb-4" data-app-selector=".mbr-section-subtitle" mbr-theme-style="display-2" mbr-if="showSubtitle">
          Header Subtitle
        </h2>
        <p class="mbr-fonts-style mbr-text mbr-white mb-4" mbr-theme-style="display-7" mbr-if="showText" data-app-selector=".mbr-text, .mbr-section-btn">California Auto Registration: Fast, Friendly, and Efficient Service.</p>
        <div class="mbr-section-btn" mbr-if="showButtons" data-toolbar="-mbrBtnMove" mbr-buttons mbr-theme-style="display-7"><a class="btn btn-white-outline" href="https://mobiri.se" data-app-placeholder="Type Text">Get Started</a></div>
      </div>
    </div>
  </div>
</section>
