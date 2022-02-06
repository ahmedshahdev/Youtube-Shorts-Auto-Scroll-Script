# Youtube-Shorts-Auto-Scroll-Script
When you will paste this script on your console then your don't need to press next button for next short this script automitic press button for your when video duration complete..

-- Code Demo
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

-- Call the control function one time
control()
