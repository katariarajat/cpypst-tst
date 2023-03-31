<script>

</script>

<div id='footer-component'>
    <div id="footer-part1">
        <svg  width=100% height=100% viewBox="0 0 955 156" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M953.015 327.272C988.032 490.876 422.584 461.14 258.903 496.173C95.2213 531.206 -65.8552 426.978 -100.872 263.374C-135.888 99.7695 30.456 39.1884 194.137 4.15544C357.819 -30.8775 917.999 163.668 953.015 327.272Z" fill="#8F2966"/>
        </svg>
            
    </div>
    <div id="footer-part2">
        <svg  width=100% height=100% viewBox="0 0 1083 293" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M1089.52 30.6142C1089.52 209.555 1079.46 635.114 900.516 635.114C721.575 635.114 0.015625 563.054 0.015625 384.114C0.015625 205.174 0.015625 242.614 261.016 172.114C736.016 531.114 1089.52 -148.326 1089.52 30.6142Z" fill="#8F2966"/>
        </svg>
    </div>
        
    <div id="footer-part3">
        <svg width=100% height=100% viewBox="0 0 361 172" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="251.516" cy="251.114" r="251" fill="#48298F"/>
        </svg>
    </div>
            
    
    
</div>

<style>
    #footer-part1{
        width: 70%;
        /* background: #8F2966; */
        mix-blend-mode: exclusion;
        filter: blur(130px);
        animation-name: image1;
        animation-duration: 2s;
        animation-iteration-count: infinite;

        /* transform: rotate(-12.08deg); */
        /* align-self: flex-start; */
    }
    
    #footer-part2{
        width: 50%;
        mix-blend-mode: exclusion;
        filter: blur(130px);
        animation-name: image2;
        animation-duration: 3s;
        animation-iteration-count: infinite;

    }
    #footer-part3{
        width: 50%;
        mix-blend-mode: exclusion;
        filter: blur(130px);
        align-self: flex-end;
        animation-name: image3;
        animation-duration: 2.5s;
        animation-iteration-count: infinite;

    }
    #footer-component{
        position: absolute;
        bottom: 1%;
        z-index: -1;
        background-color: #151517;
        width:98%;
        height: 40vh;
        display: flex;
        flex-direction: row;
        row-gap: 0px;
        /* flex-wrap: wrap; */
        justify-content: space-between;
        
        /* overflow: hidden; */
    }



    @keyframes image1 {
        0%   {width: 70%}
        12.5% { width: 65% }
        25%  { width: 60% }
        37.5% { width: 55% }
        50%  { width: 50% }
        62.5% { width: 55% }
        75% { width: 60% }
        87.5% { width: 65% }
        100% {width: 70%}
    }
    @keyframes image2 {
        0%   {width: 50%}
        12.5% { width: 55% }
        25%  { width: 60% }
        37.5% { width: 65% }
        50%  { width: 70% }
        62.5% { width: 65% }
        75% { width: 60% }
        87.5% { width: 55% }
        100% {width: 50%}
    }
    @keyframes image3{
        0%   {width: 50%}
        12.5% { width: 55% }
        25%  { width: 60% }
        37.5% { width: 65% }
        50%  { width: 70% }
        62.5% { width: 65% }
        75% { width: 60% }
        87.5% { width: 55% }
        100% {width: 50%}
    }
</style>