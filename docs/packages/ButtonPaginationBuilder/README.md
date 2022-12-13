<h1 id="buttonpaginationbuilder"><ins>ButtonPaginationBuilder</ins></h1>
<h2 id="constructor">Constructor</h2>
<div class="language-js highlighter-rouge"><div class="highlight"><pre class="highlight"><code><span class="k">new</span> <span class="nx">ButtonPaginationBuilder</span><span class="p">(</span> <span class="nx">data</span> <span class="p">);</span>
</code></pre></div></div>
<table>
  <thead>
    <tr>
      <th>PARAMETER</th>
      <th>TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DEFAULT</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>data</td>
      <td><a href="">Message</a></td>
      <td style="text-align: center">❎</td>
      <td style="text-align: center">-</td>
      <td style="text-align: center">The message</td>
    </tr>
  </tbody>
</table>

<h2 id="methods">Methods</h2>

<h3 id="setembedsembeds">.setEmbeds(<a href="">…embeds</a>)<a href="">*</a></h3>
<table>
  <thead>
    <tr>
      <th>PARAMETER</th>
      <th>TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DEFAULT</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>embeds</td>
      <td><a href="">MessageEmbed</a></td>
      <td style="text-align: center">❎</td>
      <td style="text-align: center">-</td>
      <td style="text-align: center">The embeds to set</td>
    </tr>
  </tbody>
</table>

<hr />

<h3 id="addembedsembeds">.addEmbeds(<a href="">…embeds</a>)<a href="">*</a></h3>
<table>
  <thead>
    <tr>
      <th>PARAMETER</th>
      <th>TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DEFAULT</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>embeds</td>
      <td><a href="">MessageEmbed</a></td>
      <td style="text-align: center">❎</td>
      <td style="text-align: center">-</td>
      <td style="text-align: center">The embeds to add</td>
    </tr>
  </tbody>
</table>

<hr />

<h3 id="fastskipfastskipenabled">.fastSkip(<a href="">fastSkipEnabled</a>)</h3>

<table>
  <thead>
    <tr>
      <th>PARAMETER</th>
      <th>TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DEFAULT</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>fastSkipEnabled</td>
      <td><a href="">Boolean</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">false</td>
      <td style="text-align: center">Enable/disable fastSkip</td>
    </tr>
  </tbody>
</table>

<hr />

<h3 id="settimems">.setTime(<a href="">ms</a>)</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: center">PARAMETER</th>
      <th style="text-align: center">TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DEFAULT</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center">ms</td>
      <td style="text-align: center"><a href="">Number</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">0</td>
      <td style="text-align: center">Time until the pagination expires</td>
    </tr>
  </tbody>
</table>

<hr />

<h3 id="setmaxmax">.setMax(<a href="">max</a>)</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: center">PARAMETER</th>
      <th style="text-align: center">TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DEFAULT</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center">max</td>
      <td style="text-align: center"><a href="">Number</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">0</td>
      <td style="text-align: center">Amount of clicks until pagination expires</td>
    </tr>
  </tbody>
</table>

<hr />

<h3 id="setauthoruser">.setAuthor(<a href="https://discord.com/developers/docs/resources/user">User</a>)</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: center">PARAMETER</th>
      <th style="text-align: center">TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DEFAULT</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center">User</td>
      <td style="text-align: center"><a href="https://discord.com/developers/docs/resources/user">User</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">message.author / message.user</td>
      <td style="text-align: center">Author of the pagination</td>
    </tr>
  </tbody>
</table>

<hr />

<h3 id="setchannelchannel">.setChannel(<a href="https://discord.com/developers/docs/resources/channel">Channel</a>)</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: center">PARAMETER</th>
      <th style="text-align: center">TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DEFAULT</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center">Channel</td>
      <td style="text-align: center"><a href="https://discord.com/developers/docs/resources/channel">Channel</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">message.channel</td>
      <td style="text-align: center">Channel for the pagination</td>
    </tr>
  </tbody>
</table>

<hr />

<h3 id="setcontentcontent">.setContent(<a href="">content</a>)</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: center">PARAMETER</th>
      <th style="text-align: center">TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DEFAULT</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center">content</td>
      <td style="text-align: center"><a href="">String</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">””</td>
      <td style="text-align: center">Message content</td>
    </tr>
  </tbody>
</table>

<hr />

<h3 id="replyoptionoptions-enabled">.replyOption(<a href="">options</a>, <a href="">enabled</a>)</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: center">PARAMETER</th>
      <th style="text-align: center">TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DEFAULT</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center">options</td>
      <td style="text-align: center"><a href="">Object</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">{ }</td>
      <td style="text-align: center">Reply to the message/interaction</td>
    </tr>
    <tr>
      <td style="text-align: center">enabled</td>
      <td style="text-align: center"><a href="">Boolean</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">false</td>
      <td style="text-align: center">Reply options is enabled or not</td>
    </tr>
  </tbody>
</table>

<hr />
<h3 id="setidleidle">.setIdle(<a href="">idle</a>)</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: center">PARAMETER</th>
      <th style="text-align: center">TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DEFAULT</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center">idle</td>
      <td style="text-align: center"><a href="">Boolean</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">false</td>
      <td style="text-align: center">Resets the timer on click</td>
    </tr>
  </tbody>
</table>

<hr />

<h3 id="pagetravelboolean">.pageTravel(<a href="">boolean</a>)</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: center">PARAMETER</th>
      <th style="text-align: center">TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DEFAULT</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center">boolean</td>
      <td style="text-align: center"><a href="">Boolean</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">false</td>
      <td style="text-align: center">Allows you use numbers for navigation</td>
    </tr>
  </tbody>
</table>

<hr />

<h3 id="setcomponentscomponents-event">.setComponents(<a href="">components</a>, <a href="">event</a>)</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: center">PARAMETER</th>
      <th style="text-align: center">TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center">components</td>
      <td style="text-align: center"><a href="">Array</a> / <a href="https://discord.js.org/#/docs/discord.js/stable/class/MessageActionRow">MessageActionRow</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">Allows for custom components to be added</td>
    </tr>
    <tr>
      <td style="text-align: center">collect</td>
      <td style="text-align: center"><a href="">function</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">The event for the custom components</td>
    </tr>
    <tr>
      <td style="text-align: center">end</td>
      <td style="text-align: center"><a href="">function</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">The event when the collector ends</td>
    </tr>
  </tbody>
</table>

<hr />

<h3 id="trashboolean">.trash(<a href="">Boolean</a>)</h3>

<p>| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:———:|:————-:|:———:|:——-:|:———:|
|    Boolean|<a href="">Boolean</a>   |✅          |   false  |  Adds a button to delete the current pagination.  |
—</p>
<h3 id="pagefooterboolean">.pageFooter(<a href="">Boolean</a>)</h3>
<p>| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:———:|:————-:|:———:|:——-:|:———:|
|toggle|<a href="">Boolean</a>|✅|true|Toggle the pagination footer|
—</p>

<h3 id="setbuttonsname-properties">.setButtons(<a href="">name</a>, <a href="">properties</a>)</h3>
<ul>
  <li>see <a href="https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#example">example</a></li>
  <li>ButtonNames: <a href="https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#buttonnames">Click here</a></li>
  <li>ButtonProperties: <a href="https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#buttonproperties">Click here</a></li>
</ul>

<p><a href="https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md">Click here</a> to learn how to use <code class="language-plaintext highlighter-rouge">.setButton</code></p>

<table>
  <thead>
    <tr>
      <th style="text-align: center">PARAMETER</th>
      <th style="text-align: center">TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DEFAULT</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center">name</td>
      <td style="text-align: center"><a href="">String</a> / <a href="https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#buttonnames">ButtonNames</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">” “</td>
      <td style="text-align: center">Name of the button you wish to customize</td>
    </tr>
    <tr>
      <td style="text-align: center">properties</td>
      <td style="text-align: center"><a href="">Object</a> / <a href="https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#buttonproperties">ButtonProperties</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">{ }</td>
      <td style="text-align: center">Allows you to customize button properties</td>
    </tr>
  </tbody>
</table>

<hr />

<h3 id="setfilteruser">.setFilter(<a href="https://discord.com/developers/docs/resources/user">User</a>)</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: center">PARAMETER</th>
      <th style="text-align: center">TYPE</th>
      <th style="text-align: center">OPTIONAL</th>
      <th style="text-align: center">DEFAULT</th>
      <th style="text-align: center">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center">User</td>
      <td style="text-align: center"><a href="https://discord.com/developers/docs/resources/user">User</a></td>
      <td style="text-align: center">✅</td>
      <td style="text-align: center">message.author / message.user</td>
      <td style="text-align: center">The user that can interact with the pagination</td>
    </tr>
  </tbody>
</table>
