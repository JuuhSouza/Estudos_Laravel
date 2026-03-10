## Adicionado listas no controller

&amp;lt;?php  

namespace App\Http\Controllers;

class SeriesController
{
    public function listarSeries()
    {
        $series = [
            &#39;Lost&#39;,
            &#39;Game of Thrones&#39;,
            &#39;See&#39;
        ];

        $html = &#39;&amp;lt;ul&amp;gt;&#39;;

        foreach ($series as $serie) {
            $html .= &quot;&amp;lt;li&amp;gt;$serie&amp;lt;/li&amp;gt;&quot;;
        }

        $html .= &#39;&amp;lt;/ul&amp;gt;&#39;;

        return $html;
    }
}
