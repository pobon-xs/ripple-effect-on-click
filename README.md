# Ripple Effect On CLick

    if ($('html').data("click-ripple-animation") === "yes") {
      $("html").append('<i class="ripple"></i>');
      $("html").on("mousedown", function (e) {
        $("i.ripple").addClass("active").css("left", e.pageX).css("top", e.pageY);
      });

      $("i.ripple").bind("transitionend webkitTransitionEnd oTransitionEnd MSTransitionEnd", function () {
        return $("i.ripple").removeClass("active");
      });
    }
