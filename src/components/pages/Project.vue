<template>
  <div>
    <section id="content">
      <button @click.prevent="addTaskInBacklog()">
        Add
      </button>
      <div
        class='storie'
        v-for="bkg in backlog">
          <div class="task">{{ bkg.name }}</div>
          <div>{{bkg.description}}</div>  
      </div> 
      <p>This page demonstrates a 3 column responsive layout, complete with responsive images and jquery slideshow.</p>
    </section>
    
    <section id="middle">
      <h2>2nd Content Area</h2>
      <p>At full width all three columns will be displayed side by side. As the page is resized the third column will collapse under the first and second. At the smallest screen size all three columns will be stacked on top of one another.</p>
      <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi.</p>
    </section>

    <aside id="sidebar">
      <h2>3rd Content Area</h2>
      <p>Eodem modo typi, qui nunc nobis videntur parum clari, fiant sollemnes in futurum.</p>
      <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.</p>
      <p>Eodem modo typi, qui nunc nobis videntur parum clari, fiant sollemnes in futurum.</p>
    </aside>
  </div>
</template>
<script>
export default {
  data () {
    return {
      name: 'Project',
      backlog: [],
      task: {
        name: 'Teste',
        decription: 'Teste'
      }
    }
  },
  methods: {
    addTaskInBacklog () {
      this.backlog = [...this.backlog, this.task]
    }
  }

}
</script>
<style scoped>
 @import url(https://fonts.googleapis.com/css?family=Open+Sans);

body { 
  font-family: 'Open Sans', sans-serif;
  color: #666;
}

/* STRUCTURE */


.storie {
  background: #aaaaaa;
  margin-top: 2em;
  margin-left: 2em;
  padding: 1em;
  width: 150px;
  height: 75px;
}

header {
	height: 100px;
	padding: 0 15px;
}
#content {
	width: 290px;
	float: left;
	padding: 5px 15px;
}

#middle {
	width: 294px; /* Account for margins + border values */
	float: left;
	padding: 5px 15px;
}

#sidebar {
	width: 270px;
	padding: 5px 15px;
	float: left;
}

/************************************************************************************
MEDIA QUERIES
*************************************************************************************/
/* for 980px or less */
@media screen and (max-width: 980px) {
	
	#pagewrap {
		width: 94%;
	}
	#content {
		width: 41%;
		padding: 1% 4%;
	}
	#middle {
		width: 41%;
		padding: 1% 4%;
		margin: 0px 0px 5px 5px;
		float: right;
	}
	
	#sidebar {
		clear: both;
		padding: 1% 4%;
		width: auto;
		float: none;
	}

	header, footer {
		padding: 1% 4%;
	}
}

/* for 700px or less */
@media screen and (max-width: 600px) {

	#content {
		width: auto;
		float: none;
	}
	
	#middle {
		width: auto;
		float: none;
		margin-left: 0px;
	}
	
	#sidebar {
		width: auto;
		float: none;
	}

}

/* for 480px or less */
@media screen and (max-width: 480px) {

	header {
		height: auto;
	}
	h1 {
		font-size: 2em;
	}
	#sidebar {
		display: none;
	}

}


#content {
	background: #D8DADA;
}
#middle {
  background: #747676;
}
#sidebar {
	background: #333333;
}



</style>

