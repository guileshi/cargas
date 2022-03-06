<script>

    var howWorks__group2 = document.querySelector(".howWorks__group2")

    var howWorks__group2Options = {
        root: null,

        threshold: 0,

        rootMargin: "0px"
    }


    var observerhowWorks__group2 = new IntersectionObserver(function (entries) {
        entries.forEach(entry => {
            if (entry.isIntersecting && entry.target === howWorks__group2) {
                
                document.querySelector(".howWorks__group2").classList.add('teste')

            } 
        })
    }, howWorks__group2Options);

    if(howWorks__group2){
        observerhowWorks__group2.observe(howWorks__group2)
    }

</script>