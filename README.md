# bbd_chopper.ee_addon
A Build of the old Hacksaw plugin for EE3 since it was let go.

<a href='https://pledgie.com/campaigns/32205'><img alt='Click here to lend your support to: ExpressionEngine Chopper Addon and make a donation at pledgie.com !' src='https://pledgie.com/campaigns/32205.png?skin_name=chrome' border='0' ></a>

If you ever used Brett DeWoody's EE Hacksaw, then you were probably sad to see it was labeled INACTIVE. I know I was. That's why I revived it in an ExpressionEngine 3 friendly version.

All of the functionality remains the same as it did with the older versions in EE2.

Chopper takes your entry's content and whittles it down to a more manageable size. It strips the HTML and limits the excerpts by character count, word count or cutoff marker.
To use Chopper simply wrap the content you want to truncate with the exp:chopper tag, like this:
<pre><code>&#123;exp:chopper&#125;
   &#123;your_content&#125;
&#123;/exp:chopper&#125;
</code></pre>

There are several parameters you can use to control how the content is truncated. These options are:

chars   = ""     // Limit by number of characters
words   = ""     // Limit by number of words
cutoff = ""      // Limit by a specific cutoff string
append = ""      // String to append to the end of the excerpt
allow   = ""     // HTML tags you want to allow. Ex allow="<b><a>"

For example, if you want to limit your excerpt to 100 words you would do this:

<pre><code>&#123;exp:chopper words="100"&#125;
   &#123;your_content&#125;
&#123;/exp:chopper&#125;
</code></pre>

By default Chopper will strip all HTML from your excerpt. If you would like to keep some basic HTML you can use the "allow" parameter to keep specific HTML tags. For example, let's say you want to keep <code>&lt;p&gt;</code> and <code>&lt;b&gt;</code> tags:

<pre><code>&#123;exp:chopper words="100" allow="&lt;p&gt;&lt;b&gt;"&#125;
   &#123;your_content&#125;
&#123;/exp:chopper&#125;
</code></pre>

This would strip all HTML except paragraph (<code>&lt;p&gt;</code>) and bold (<code>&lt;b&gt;</code>) tags.

Another way to limit content is by a cutoff string. This is similar to the way Wordpress's "more" feature works. In your content you could add a specific string to indicate the spot you want the excerpt to stop. Let's say you use "<code>&lt;!--END--&gt;</code>". To cut the excerpt off at this location you would do this:

<pre><code>&#123;exp:chopper cutoff="&lt;!-- END --&gt;"&#125;
   &#123;your_content&#125;
&#123;/exp:chopper&#125;</code></pre>

The "cutoff" parameter can be coupled with the "words" parameter in case you forget to add the cutoff string to some of your entries. This way the excerpt will be truncated at the cutoff string, OR after X words.

You can add any string at the end of the excerpt using the "append" parameter, like this:

<pre><code>&#123;exp:chopper words="100" append="..."&#125;
   &#123;your_content&#125;
&#123;/exp:chopper&#125;
</code></pre>

This would append "..." to the end of the excerpt.

I am not sure what all other addons this will work with right now since there are so few ready for EE3 right now. 
