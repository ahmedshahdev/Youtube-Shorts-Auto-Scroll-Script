function control() {
    const interval = setInterval(() => {
        var ele = document.querySelector('[data-no-fullscreen="true"]')
        var duration = parseInt(ele.duration);
        var current_duration = parseInt(ele.currentTime);
        if (current_duration == duration) {
            clearInterval(interval);
            setTimeout(()=>{
                let btn = document.querySelector(".navigation-button").nextElementSibling;
                btn.querySelector("button").click()
                control()
            }, 500)
        } 
    });
}

control()
