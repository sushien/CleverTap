// Empty constructor
function clevertap() {}

// The function that passes work along to native shells
// Message is a string, duration may be 'long' or 'short'
clevertap.prototype.show = function(message, duration, successCallback, errorCallback) {
  var options = {};
  options.message = message;
  options.duration = duration;
  cordova.exec(successCallback, errorCallback, 'clevertap', 'show', [options]);
}

// Installation constructor that binds clevertap to window
clevertap.install = function() {
  if (!window.plugins) {
    window.plugins = {};
  }
  window.plugins.clevertap = new clevertap();
  return window.plugins.clevertap;
};
cordova.addConstructor(clevertap.install);