babel.config.js 작성 구문에서 api.cache 의 의미

module.exports = function(api) {
  api.cache(true);
  return {
    presets: ['babel-preset-expo'],
  };
};

보통 위와 같이 설정한다. 

Babel config를 JS 파일로 작성할 경우, 'Production'이나 'Development' 환경에 따라 그 환경을 다르게 구성하는것에 용이 하다.
ex )  process.env.NODE_ENV === 'production' ? ['transform-remove-console'] : [],
 
반면에, 캐싱이 더 어려워 지는 단점이 있다. 파일이 새로 컴파일 될때마다 바벨은 이 config function을 재실행하는데, 이는 프로그램의 속도에 영향을 준다.
그렇기 때문에, 이는 config 파일 내에 설정된 plugin과 presets 다시 호출하게 되고 이는 프로그램의 속도에 영향을 준다. 

이러한 속도 저하를 피하기 위해서, 바벨은 config function내에서 유저가 직접 cache 처리를 어떻게 할것인지에 대한 함수를 제공한다. 

api.cache.forever() - config를 한번만 로드한다. (캐싱 처리)
api.cache.never() - config 를 캐쉬하지 않고, 매번 실행한다. 
api.cache(true) - api.cache.forever()
api.cache(false) -  api.cache.never()
Since the actual callback result is used to check if the cache entry is valid, it is recommended that:


https://babeljs.io/docs/en/config-files#apicache
에서 부분 발췌
