##  Kopiera

<pre><code class="javascript">
	
	var x = $('.class').clone();

	$('span').prepend(x);

	/* ELLER */

	$('span').prepend($('.class').clone());

	/* BONUS! */
	$('.class').clone(true);

</code></pre>


<div class="readmore">
<i class="fa fa-book"></i> [https://api.jquery.com/category/selectors/child-filter-selectors/](https://api.jquery.com/category/selectors/child-filter-selectors/)	
</div>
