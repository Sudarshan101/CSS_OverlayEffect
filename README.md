# CSS_OverlayEffect
Overlay Effect on the image using CSS and data attribute

# overlay.html
<pre>
  <h1>Overlay Effect on the image using CSS and data attribute</h1>
		<div class="section" data-overlay="black" data-opacity="65">
			<div class="content">
				<h3>Content Title</h3>
				<h5>Content Sub Title</h5>
				<p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
			</div>
		</div>
</pre>

# style.css
<pre>
  .section{
				background:url('push-notification-ios10.jpg') no-repeat center;
				padding:60px 0;
				position:relative;
			}
			.section .content{
				position:relative;
			}
			[data-overlay] {
				position: relative;
				background-size: cover;
				background-repeat: no-repeat;
				background-position: center center;
			}
			[data-overlay]::before {
				position: absolute;
				left: 0;
				top: 0;
				right: 0;
				bottom: 0;
				content: "";
			}
			[data-overlay="black"]::before {
				background-color: #000000;
			}
			[data-opacity="65"]::before {
				opacity: 0.65;
			}
			.section .content h3{
				color: #fff;
				font-size: 3rem;
				text-align: center;
				margin:10px;
			}
			.section .content h5{
				color: #fff;
				font-size: 2rem;
				margin:10px;
				text-align: center;
			}
			.section .content p{
				color: #fff;
				font-size: 1.2rem;
				margin:10px;
				text-align: center;
			}
</pre>

# Preview
<img src="https://github.com/Sudarshan101/CSS_OverlayEffect/blob/master/Screenshot_1.png" style="width:100%;" />
