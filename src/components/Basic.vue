<template>
  <div class="basic">
    <h1>Заголовок 1</h1>
    <h2>Заголовок 2</h2>
    <h3>Заголовок 3</h3>
    <h4>Заголовок 4</h4>
    <h5>Заголовок 5</h5>
    <h6>Заголовок 6</h6>
    <p>Параграф</p>
    <ol>
      <li>
        Пункт 1
        <ol>
          <li>Подпункт 1</li>
          <li>Подпункт 2</li>
        </ol>
      </li>
      <li>Пункт 2</li>
      <li>Пункт 3</li>
    </ol>

    <ul>
      <li>
        Пункт 1
        <ul>
          <li>Подпункт 1</li>
          <li>Подпункт 2</li>
        </ul>
      </li>
      <li>Пункт 2</li>
      <li>Пункт 3</li>
    </ul>

    <dl>
      <dt>Термин 1</dt>
        <dd>Определение термина 1</dd>
      <dt>Термин 2</dt>
        <dd>Определение термина 2</dd>
    </dl>

    <hr>
    <table>
      <tr>
        <td><code>&lt;a&gt;</code></td>
        <td><a href="#">ссылка</a></td>
      </tr>
      <tr>
        <td><code>&lt;strong&gt;</code></td>
        <td><strong>действительно значимый текст</strong></td>
      </tr>
      <tr>
        <td><code>&lt;b&gt;</code></td>
        <td><b>просто выделенный текст</b></td>
      </tr>
      <tr>
        <td><code>&lt;i&gt;</code></td>
        <td><i>иностранное слово или термин</i></td>
      </tr>
      <tr>
        <td><code>&lt;em&gt;</code></td>
        <td><em>акцентирование текста</em></td>
      </tr>
      <tr>
        <td><code>&lt;del&gt;</code></td>
        <td><del>текст, который был удален</del></td>
      </tr>
      <tr>
        <td><code>&lt;ins&gt;</code></td>
        <td><ins>текст, который был добавлен</ins></td>
      </tr>
      <tr>
        <td><code>&lt;small&gt;</code></td>
        <td><small>малозначимый текст</small></td>
      </tr>
      <tr>
        <td><code>&lt;abbr&gt;</code></td>
        <td><abbr title="расшифровка аббревиатуры">аббревиатура</abbr></td>
      </tr>
      <tr>
        <td><code>&lt;kbd&gt;</code></td>
        <td><kbd title="обозначения текста, который набирается на клавиатуре">alt + 2</kbd></td>
      </tr>
      <tr>
        <td><code>&lt;sup&gt;</code></td>
        <td>H<sup>1+</sup></td>
      </tr>
      <tr>
        <td><code>&lt;sub&gt;</code></td>
        <td>H<sub>2</sub></td>
      </tr>
      <tr>
        <td><code>&lt;code&gt;</code></td>
        <td><code>color: red</code></td>
      </tr>
      <tr>
        <td><code>&lt;header&gt;</code></td>
        <td><header>шапка сайта</header></td>
      </tr>
      <tr>
        <td><code>&lt;nav&gt;</code></td>
        <td><nav>навигация</nav></td>
      </tr>
      <tr>
        <td><code>&lt;aside&gt;</code></td>
        <td><aside>блок сбоку от контента для размещения рубрик, ссылок на архив, меток</aside></td>
      </tr>
      <tr>
      <tr>
        <td><code>&lt;main&gt;</code></td>
        <td><main>основной контент</main></td>
      </tr>
      <tr>
        <td><code>&lt;section&gt;</code></td>
        <td><section>раздел документа, обычно содержит заголовок</section></td>
      </tr>
      <tr>
        <td><code>&lt;article&gt;</code></td>
        <td><article>раздел вроде новости, статьи, записи блога, форума</article></td>
      </tr>
      <tr>
        <td><code>&lt;footer&gt;</code></td>
        <td><footer>подвал сайта</footer></td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: 'Basic',
}
</script>

<style scoped lang="scss">

</style>
