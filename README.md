<table class="chaarts radar-multiple" id="radar-multiple" style="--scale: 20; --step: 5; --items: 7; --areas: 2;">
  <caption id="caption-9">[…]</caption>
  <thead>
    <tr>
      <th scope="col">[…]</th>
      <th scope="col">[…]</th>
    </tr>
  </thead>
  <tbody>
    <tr style="--color: #734bf9; --1: 14; --2: 11; --3: 13; --4: 16; --5: 14; --6: 10; --7: 4; --8: var(--1);">
      <th scope="row">Gaël</th>
      <td><span>14</span></td>
    </tr>
    <tr style="-color: #e11a81; --1: 18; --2: 10; --3: 11; --4: 16; --5: 10; --6: 12; --7: 11; --8: var(--1);">
      <th scope="row">Luc</th>
      <td><span>18</span></td>
    </tr>
  </tbody>
</table>
<style>
	.chaarts.radar-multiple {
  margin-bottom: 12rem;
}

.chaarts.radar-multiple tbody {
  columns: var(--areas);
  vertical-align: bottom;
}

.chaarts.radar-multiple [scope="row"] {
  bottom: -8rem;
  height: 2rem;
  left: 1rem;
  position: absolute;
}

.chaarts.radar-multiple [scope="row"]::before {
  background: var(--color, currentColor);
  content: "";
  display: inline-block;
  height: 1rem;
  margin-right: .25rem;
  transform: translate3d(0, .1rem, 0);
  width: 1rem;
}

/* 2nd: */
.chaarts.radar-multiple tr:nth-child(2) [scope="row"] {
  left: calc( 1rem + (100% / var(--areas)) * 1);
}

.chaarts.radar-multiple td {
  align-items: flex-end;
  border-color: var(--color, currentColor);
  display: flex;
  justify-content: flex-end;
  opacity: .5;
  pointer-events: none;
  transition: opacity .2s cubic-bezier(.5, 0, .5, 1);
  z-index: 0;
}

.chaarts.radar-multiple td::after {
  color: var(--color, currentColor);
  display: block;
  font-size: small;
  font-weight: 700;
  text-indent: -.5rem;
  transform:
    skew( calc( var(--skew) * -1 ) )
    rotate( calc( var(--part) * var(--index, 1) * -1 ) );
  transform-origin: 0 0;
  width: 100%;
  white-space: nowrap;
}

.chaarts.radar-multiple td:nth-of-type(2)::after {
  --integer: calc(var(--2));
  counter-reset: value var(--integer);
  content: counter(value);
  width: calc( var(--2) * 100% / var(--scale) );
}

.chaarts.radar-multiple span {
  background: var(--color, currentColor);
  pointer-events: auto;
}

@supports (mask-image: url()) {
  .chaarts.radar-multiple span {
    --mask: radial-gradient(circle at bottom right, rgba(0,0,0,1), rgba(0,0,0,.5));
    mask-image: var(--mask);
  }
}

@media (hover: hover) {
  .chaarts.radar-multiple td {
    opacity: .25;
  }

  .chaarts.radar-multiple td::after {
    opacity: 0;
  }

  .chaarts.radar-multiple tr:hover td {
    opacity: 1;
    z-index: 1;
  }

  .chaarts.radar-multiple tr:hover td::after {
    opacity: inherit;
  }
}
</style>
