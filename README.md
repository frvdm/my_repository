my_repository
=============

 //
    // 1.
    // This doesn't work like you might think, because the value of 'i' never
    // gets locked in. Instead, every link, when clicked (well after the loop
    // has finished executing), alerts the total number of elements, because
    // that's what the value of `i` actually is at that point.
    //

    window.onload = function () {
      var elems = document.getElementsByTagName('a');

      for (var i = 0; i < elems.length; i++) {

        elems[i].addEventListener('click', function (e) {
          e.preventDefault();
          alert('I am link #' + i);
        }, 'false');

      }

    }
