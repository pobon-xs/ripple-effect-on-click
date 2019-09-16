# Ripple Effect On CLick

## jQuery
    if ($('html').data("click-ripple-animation") === "yes") {
      $("html").append('<i class="ripple"></i>');
      $("html").on("mousedown", function (e) {
        $("i.ripple").addClass("active").css("left", e.pageX).css("top", e.pageY);
      });

      $("i.ripple").bind("transitionend webkitTransitionEnd oTransitionEnd MSTransitionEnd", function () {
        return $("i.ripple").removeClass("active");
      });
    }

## CSS
    i.ripple {
        position: absolute;
        height: 60px;
        width: 60px;
        background: #fff;
        margin: -30px;
        border-radius: 100%;
        opacity: 1;
        transform: scale(0);
        z-index: 9999;
        user-select: none;
        pointer-events: none;
    }
