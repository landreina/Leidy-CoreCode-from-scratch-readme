# ASCII Total

>### function uniTotal (string) {
  let long = string.length;
  let suma = 0;
  for (let i = 0; i < long; i++){
    suma = suma + string.charCodeAt(i);
  }
  return suma;
}
>
