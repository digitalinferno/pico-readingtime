<?php
/**
 * Pico reading time plugin.
 *
 * PicoReadingTime allows you to easily add an estimated reading time to your
 * page's content. The plugin is enabled by default, and the time is displayed
 * in minutes. To add the reading time to your page, simply add { ReadingTime }
 * inside your tpl file.
 *
 * @author  Giovanni Forte <giovanni@teamvodka.eu>
 * @link    https://teamvodka.eu
 * @license https://opensource.org/licenses/MIT The MIT License
 * @version 0.9
 */
class PicoReadingTime extends AbstractPicoPlugin {

    const API_VERSION = 3;
    protected $enabled = true;   
  
    public function onContentLoaded(&$content)
    {
        $words = str_word_count(strip_tags($content));
        $time = ceil($words / 238);
        $this->read = $time;
    }

    public function  onPageRendering(&$twig, &$twigVariables)
    {
  	    $twigVariables['ReadingTime']  =  $this->read;
    }

}
?>
