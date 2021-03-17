# UI components library
<ul>
<li>Elements
	<ul>
		<li><a href='#card'>Card</a></li>
		<li><a href='#modal'>Modal</a></li>
		<li><a href='#tab'>Tab</a></li>
		<li><a href='#dropdown-menu'>Dropdown-menu</a></li>
		<li><a href='#accordion'>Accordion</a></li>
		<li><a href='#slider'>Slider</a></li>
	</ul>
</li>
<li>Methods
	<ul>
		<li><a href='#requests'>Requests</a></li>
		<li><a href='#actions'>Actions</a></li>
		<li><a href='#attributes'>Attributes</a></li>
		<li><a href='#classes'>Classes</a></li>
		<li><a href='#effects'>Effects</a></li>
		<li><a href='#handlers'>Handlers</a></li>
	</ul>
</li>

	
</ol>

## Card

    <div  class="card mr20">
	    <img  src=""  class="card-img">
	    <div  class="card-body">
		    <div  class="card-content">
			    <h3  class="card-title">Title</h3>
			    <p  class="card-text">...</p>
		    </div>
		    <a  href="#"  class="btn btn-primary"  data-toggle='modal'  data-target='#exampleModal'>Click</a>
	    </div>
    </div>
## Modal

    <div  class="modal"  id="exampleModal">
	    <div  class="modal-dialog">
		    <div  class="modal-content">
			    <button  class="close"  data-close>
				    <span>&times;</span>
			    </button>
			    <div  class="modal-header">
				    <h3  class="modal-title">Modal Title</h3>
			    </div>
			    <div  class="modal-body">Modal Body</div>
			    <div  class="modal-footer">
				    <button  class="btn btn-danger"  data-close>Close</button>
				    <button  class="btn btn-success">Save Changes</button>
			    </div>
		    </div>    
	    </div>
    </div>

**Modal initialization:**

    $('[data-toggle="modal"]').modal();
   or
   

    $("[data-target='#myModal']").click(()  =>  {
	    $("[data-target='#myModal']").createModal({ 
		    text:  {
		    title:  'Modal title',
		    body:  'Modal body text'
		    },
		    btns:  {
			    count:  2,  // Number of buttons
			    settings: [
				    [
					    'close',  // Button text
					    [ 'btn-danger',  'mr10' ],  // Classes
					    true,  // Is it close button?
				    ],
				    [
					    'open',
					    [ 'btn-dark' ],
					    false,
					    ()  =>  alert('you did it!'),
				    ]
			    ]
		    }
	    })
	});
# Tab
    <div  class="tab">
	    <div  class="tab-panel"  data-tabpanel>
		    <div  class="tab-item tab-item--active">...</div>
		    <div  class="tab-item">...</div>
		    <div  class="tab-item">...</div>
	    </div>
	    <div  class="tab-content tab-content--active">...</div>
	    <div  class="tab-content">...</div>
	    <div  class="tab-content">...</div>
    </div>
**Tab initialization:**

    $('[data-tabpanel] .tab-item').tab();

## Dropdown-menu

    <div  class="dropdown">
	    <button  id="dropDownMenuId"  class="dropdown-trigger btn btn-primary mt10">Dropdown Menu</button>
	    <div  class="dropdown-menu" data-toggle-id='dropDownMenuId'>
		    <a  href=""  class="dropdown-item">Link</a>
		    <a  href=""  class="dropdown-item">Link 2</a>
		    <a  href=""  class="dropdown-item">Link 3</a>
	    </div>
    </div>
  **Dropdown-menu initialization:**

      $('.dropdown-trigger').dropdown();
## Accordion

    <div  class="accordion">
	    <div  class="accordion-header">...</div>
	    <div  class="accordion-content">
		    <div  class="accordion-inner">...</div>
		</div>
    </div>
	<div  class="accordion">
	    <div  class="accordion-header accordion-header--active">...</div>
	    <div  class="accordion-content accordion-content--active">
		    <div  class="accordion-inner">...</div>
	    </div>
    </div>
  **Accordion initialization:**
  

    $('.accordion-header').accordion();
## Slider
	<div class="carousel">
		<ol class="carousel-indicators">
			<li class="active" data-slide-to='0'></li>
			<li data-slide-to='1'></li>
			<li data-slide-to='2'></li>
		</ol>
		<div class="carousel-inner">
			<div class="carousel-slides">
				<div class="carousel-item">
					<img src="" alt="">
					<h4>...</h4>
				</div>
				<div class="carousel-item">
					<img src="" alt="">
					<h4>...</h4>
				</div>
				<div class="carousel-item">
					<img src="" alt="">
					<h4>...</h4>
				</div>
			</div>
		</div>
		<a href="#" class="carousel-prev" data-slide='prev'>
			<span class="carousel-prev-icon">&lt;</span>
		</a>
		<a href="#" class="carousel-next" data-slide='prev'>
			<span class="carousel-next-icon">&gt;</span>
		</a>
	</div>
**Slider initialization:**

    $('.carousel').carousel({
    	autoplay: false,
    	slidesForOneTime: 1,
    	slidesOnPage: 1,
    	oneSide: false,
    });

or

    $().createCarousel({
    	slidesInfo: [
    		[
    			src,
    			text,
    		],
    		[
    			src,
    			text,
    		],
    	],
    	autoplay: true,
    	slidesForOneTime: 1,
    	slidesOnPage: 2,
    	oneSide: true,
    	links: false,
    });

## Requests
**Get:**
	

    $().get(url, dataTypeAnswer);

**Post:**

    $().post(url, data, dataTypeAnswer); 
    

## Actions

    $(selector).html(text);
    $(selector).eq(index);
    $(selector).index();
    $(selector).find(selector);
    $(selector).siblings();
    $(selector).closest(selector);
  
  ## Attributes

    $(selector).attr(name, value);
    $(selector).removeAttr(name);
  ## Classes

    $(selector).addClass(className);
    $(selector).removeClass(className);
    $(selector).toggleClass(className);
  ## Display

    $(selector).show();
    $(selector).hide();
    $(selector).toggle();
   ## Effects

    $(selector).fadeIn(duration,  display,  function);
    $(selector).fadeOut(duration,  function);
    $(selector).fadeToggle(duration,  display,  function);
  
   ## Handlers

    $(selector).on(event,  callback);
    $(selector).off(event,  callback);
    $(selector).click(handler);
  
    
