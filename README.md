# api documentation for  [statsd (v0.8.0)](https://github.com/etsy/statsd)  [![npm package](https://img.shields.io/npm/v/npmdoc-statsd.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-statsd) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-statsd.svg)](https://travis-ci.org/npmdoc/node-npmdoc-statsd)
#### Network daemon for the collection and aggregation of realtime application metrics

[![NPM](https://nodei.co/npm/statsd.png?downloads=true)](https://www.npmjs.com/package/statsd)

[![apidoc](https://npmdoc.github.io/node-npmdoc-statsd/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-statsd_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-statsd/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-statsd/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Etsy",
        "url": "https://codeascraft.com"
    },
    "bin": {
        "statsd": "./bin/statsd"
    },
    "bugs": {
        "url": "https://github.com/etsy/statsd/issues"
    },
    "dependencies": {
        "generic-pool": "2.2.0",
        "hashring": "3.2.0",
        "modern-syslog": "1.1.2",
        "winser": "=0.1.6"
    },
    "description": "Network daemon for the collection and aggregation of realtime application metrics",
    "devDependencies": {
        "nodeunit": "0.9.x",
        "temp": "0.4.x",
        "underscore": "1.4.x"
    },
    "directories": {},
    "dist": {
        "shasum": "92041479e174a214df7147f2fab1348af0839052",
        "tarball": "https://registry.npmjs.org/statsd/-/statsd-0.8.0.tgz"
    },
    "engines": {
        "node": ">=0.10"
    },
    "gitHead": "5d729d95847db0189e2c5571014b54c63d661f31",
    "homepage": "https://github.com/etsy/statsd",
    "keywords": [
        "statsd",
        "etsy",
        "metric",
        "aggregation",
        "realtime"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "kastner",
            "email": "kastner@gmail.com"
        },
        {
            "name": "mrtazz",
            "email": "d@unwiredcouch.com"
        },
        {
            "name": "draco2003",
            "email": "dan@dracosplace.com"
        },
        {
            "name": "pkhzzrd",
            "email": "pk.hzzrd@gmail.com"
        }
    ],
    "name": "statsd",
    "optionalDependencies": {
        "hashring": "3.2.0",
        "modern-syslog": "1.1.2",
        "winser": "=0.1.6"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/etsy/statsd.git"
    },
    "scripts": {
        "install-windows-service": "winser -i",
        "start": "node stats.js config.js",
        "test": "./run_tests.sh",
        "uninstall-windows-service": "winser -r"
    },
    "version": "0.8.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module statsd](#apidoc.module.statsd)
1.  object <span class="apidocSignatureSpan">statsd.</span>config
1.  object <span class="apidocSignatureSpan">statsd.</span>console
1.  object <span class="apidocSignatureSpan">statsd.</span>graphite
1.  object <span class="apidocSignatureSpan">statsd.</span>helpers
1.  object <span class="apidocSignatureSpan">statsd.</span>logger
1.  object <span class="apidocSignatureSpan">statsd.</span>mgmt_console
1.  object <span class="apidocSignatureSpan">statsd.</span>mgmt_server
1.  object <span class="apidocSignatureSpan">statsd.</span>process_metrics
1.  object <span class="apidocSignatureSpan">statsd.</span>process_mgmt
1.  object <span class="apidocSignatureSpan">statsd.</span>repeater
1.  object <span class="apidocSignatureSpan">statsd.</span>set
1.  object <span class="apidocSignatureSpan">statsd.</span>tcp
1.  object <span class="apidocSignatureSpan">statsd.</span>udp

#### [module statsd.config](#apidoc.module.statsd.config)
1.  [function <span class="apidocSignatureSpan">statsd.config.</span>Configurator (file)](#apidoc.element.statsd.config.Configurator)
1.  [function <span class="apidocSignatureSpan">statsd.config.</span>configFile (file, callbackFunc)](#apidoc.element.statsd.config.configFile)

#### [module statsd.console](#apidoc.module.statsd.console)
1.  [function <span class="apidocSignatureSpan">statsd.console.</span>init (startupTime, config, events)](#apidoc.element.statsd.console.init)

#### [module statsd.graphite](#apidoc.module.statsd.graphite)
1.  [function <span class="apidocSignatureSpan">statsd.graphite.</span>init (startup_time, config, events, logger)](#apidoc.element.statsd.graphite.init)

#### [module statsd.helpers](#apidoc.module.statsd.helpers)
1.  [function <span class="apidocSignatureSpan">statsd.helpers.</span>is_valid_packet (fields)](#apidoc.element.statsd.helpers.is_valid_packet)
1.  [function <span class="apidocSignatureSpan">statsd.helpers.</span>writeConfig (config, stream)](#apidoc.element.statsd.helpers.writeConfig)

#### [module statsd.logger](#apidoc.module.statsd.logger)
1.  [function <span class="apidocSignatureSpan">statsd.logger.</span>Logger (config)](#apidoc.element.statsd.logger.Logger)

#### [module statsd.mgmt_console](#apidoc.module.statsd.mgmt_console)
1.  [function <span class="apidocSignatureSpan">statsd.mgmt_console.</span>delete_stats (stats_type, cmdline, stream)](#apidoc.element.statsd.mgmt_console.delete_stats)
1.  [function <span class="apidocSignatureSpan">statsd.mgmt_console.</span>existing_stats (stats_type, bucket)](#apidoc.element.statsd.mgmt_console.existing_stats)

#### [module statsd.mgmt_server](#apidoc.module.statsd.mgmt_server)
1.  [function <span class="apidocSignatureSpan">statsd.mgmt_server.</span>start (config, on_data_callback, on_error_callback)](#apidoc.element.statsd.mgmt_server.start)

#### [module statsd.process_metrics](#apidoc.module.statsd.process_metrics)
1.  [function <span class="apidocSignatureSpan">statsd.</span>process_metrics (metrics, flushInterval, ts, flushCallback)](#apidoc.element.statsd.process_metrics.process_metrics)

#### [module statsd.process_mgmt](#apidoc.module.statsd.process_mgmt)
1.  [function <span class="apidocSignatureSpan">statsd.process_mgmt.</span>init (config)](#apidoc.element.statsd.process_mgmt.init)
1.  [function <span class="apidocSignatureSpan">statsd.process_mgmt.</span>set_title (config)](#apidoc.element.statsd.process_mgmt.set_title)

#### [module statsd.repeater](#apidoc.module.statsd.repeater)
1.  [function <span class="apidocSignatureSpan">statsd.repeater.</span>init (startupTime, config, emitter, logger)](#apidoc.element.statsd.repeater.init)
1.  [function <span class="apidocSignatureSpan">statsd.repeater.</span>stop (cb)](#apidoc.element.statsd.repeater.stop)

#### [module statsd.set](#apidoc.module.statsd.set)
1.  [function <span class="apidocSignatureSpan">statsd.set.</span>Set ()](#apidoc.element.statsd.set.Set)

#### [module statsd.tcp](#apidoc.module.statsd.tcp)
1.  [function <span class="apidocSignatureSpan">statsd.tcp.</span>start (config, callback)](#apidoc.element.statsd.tcp.start)

#### [module statsd.udp](#apidoc.module.statsd.udp)
1.  [function <span class="apidocSignatureSpan">statsd.udp.</span>start (config, callback)](#apidoc.element.statsd.udp.start)



# <a name="apidoc.module.statsd"></a>[module statsd](#apidoc.module.statsd)



# <a name="apidoc.module.statsd.config"></a>[module statsd.config](#apidoc.module.statsd.config)

#### <a name="apidoc.element.statsd.config.Configurator"></a>[function <span class="apidocSignatureSpan">statsd.config.</span>Configurator (file)](#apidoc.element.statsd.config.Configurator)
- description and source-code
```javascript
Configurator = function (file) {

  var self = this;
  var config = {};
  var oldConfig = {};

  this.updateConfig = function () {
    util.log('[' + process.pid + '] reading config file: ' + file);

    fs.readFile(file, function (err, data) {
      if (err) { throw err; }
      old_config = self.config;

      self.config = eval('config = ' + data);
      self.emit('configChanged', self.config);
    });
  };

  this.updateConfig();

  fs.watch(file, function (event, filename) {
    if (event == 'change' && self.config.automaticConfigReload != false) {
      self.updateConfig();
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.statsd.config.configFile"></a>[function <span class="apidocSignatureSpan">statsd.config.</span>configFile (file, callbackFunc)](#apidoc.element.statsd.config.configFile)
- description and source-code
```javascript
configFile = function (file, callbackFunc) {
  var config = new Configurator(file);
  config.on('configChanged', function() {
    callbackFunc(config.config, config.oldConfig);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.statsd.console"></a>[module statsd.console](#apidoc.module.statsd.console)

#### <a name="apidoc.element.statsd.console.init"></a>[function <span class="apidocSignatureSpan">statsd.console.</span>init (startupTime, config, events)](#apidoc.element.statsd.console.init)
- description and source-code
```javascript
init = function (startupTime, config, events) {
  var instance = new ConsoleBackend(startupTime, config, events);
  return true;
}
```
- example usage
```shell
...
  this.backend = this.config.backend || 'stdout';
  this.level   = this.config.level || "LOG_INFO";
  if (this.backend == 'stdout') {
    this.util = require('util');
  } else {
    if (this.backend == 'syslog') {
      this.util = require('modern-syslog');
      this.util.init(config.application || 'statsd', this.util.LOG_PID | this.util.LOG_ODELAY, this.util.LOG_LOCAL0);
    } else {
      throw "Logger: Should be 'stdout' or 'syslog'.";
    }
  }
};

Logger.prototype = {
...
```



# <a name="apidoc.module.statsd.graphite"></a>[module statsd.graphite](#apidoc.module.statsd.graphite)

#### <a name="apidoc.element.statsd.graphite.init"></a>[function <span class="apidocSignatureSpan">statsd.graphite.</span>init (startup_time, config, events, logger)](#apidoc.element.statsd.graphite.init)
- description and source-code
```javascript
function graphite_init(startup_time, config, events, logger) {
  debug = config.debug;
  l = logger;
  graphiteHost = config.graphiteHost;
  graphitePort = config.graphitePort || 2003;
  graphitePicklePort = config.graphitePicklePort || 2004;
  graphiteProtocol = config.graphiteProtocol || 'text';
  config.graphite = config.graphite || {};
  globalPrefix    = config.graphite.globalPrefix;
  prefixCounter   = config.graphite.prefixCounter;
  prefixTimer     = config.graphite.prefixTimer;
  prefixGauge     = config.graphite.prefixGauge;
  prefixSet       = config.graphite.prefixSet;
  globalSuffix    = config.graphite.globalSuffix;
  legacyNamespace = config.graphite.legacyNamespace;
  prefixStats     = config.prefixStats;

  // set defaults for prefixes & suffix
  globalPrefix  = globalPrefix !== undefined ? globalPrefix : "stats";
  prefixCounter = prefixCounter !== undefined ? prefixCounter : "counters";
  prefixTimer   = prefixTimer !== undefined ? prefixTimer : "timers";
  prefixGauge   = prefixGauge !== undefined ? prefixGauge : "gauges";
  prefixSet     = prefixSet !== undefined ? prefixSet : "sets";
  prefixStats   = prefixStats !== undefined ? prefixStats : "statsd";
  legacyNamespace = legacyNamespace !== undefined ? legacyNamespace : true;

  // In order to unconditionally add this string, it either needs to be an
  // empty string if it was unset, OR prefixed by a . if it was set.
  globalSuffix  = globalSuffix !== undefined ? '.' + globalSuffix : '';

  if (legacyNamespace === false) {
    if (globalPrefix !== "") {
      globalNamespace.push(globalPrefix);
      counterNamespace.push(globalPrefix);
      timerNamespace.push(globalPrefix);
      gaugesNamespace.push(globalPrefix);
      setsNamespace.push(globalPrefix);
    }

    if (prefixCounter !== "") {
      counterNamespace.push(prefixCounter);
    }
    if (prefixTimer !== "") {
      timerNamespace.push(prefixTimer);
    }
    if (prefixGauge !== "") {
      gaugesNamespace.push(prefixGauge);
    }
    if (prefixSet !== "") {
      setsNamespace.push(prefixSet);
    }
  } else {
      globalNamespace = ['stats'];
      counterNamespace = ['stats'];
      timerNamespace = ['stats', 'timers'];
      gaugesNamespace = ['stats', 'gauges'];
      setsNamespace = ['stats', 'sets'];
  }

  graphiteStats.last_flush = startup_time;
  graphiteStats.last_exception = startup_time;
  graphiteStats.flush_time = 0;
  graphiteStats.flush_length = 0;

  if (config.keyNameSanitize !== undefined) {
    globalKeySanitize = config.keyNameSanitize;
  }

  flushInterval = config.flushInterval;

  flush_counts = typeof(config.flush_counts) === "undefined" ? true : config.flush_counts;

  events.on('flush', flush_stats);
  events.on('status', backend_status);

  return true;
}
```
- example usage
```shell
...
  this.backend = this.config.backend || 'stdout';
  this.level   = this.config.level || "LOG_INFO";
  if (this.backend == 'stdout') {
    this.util = require('util');
  } else {
    if (this.backend == 'syslog') {
      this.util = require('modern-syslog');
      this.util.init(config.application || 'statsd', this.util.LOG_PID | this.util.LOG_ODELAY, this.util.LOG_LOCAL0);
    } else {
      throw "Logger: Should be 'stdout' or 'syslog'.";
    }
  }
};

Logger.prototype = {
...
```



# <a name="apidoc.module.statsd.helpers"></a>[module statsd.helpers](#apidoc.module.statsd.helpers)

#### <a name="apidoc.element.statsd.helpers.is_valid_packet"></a>[function <span class="apidocSignatureSpan">statsd.helpers.</span>is_valid_packet (fields)](#apidoc.element.statsd.helpers.is_valid_packet)
- description and source-code
```javascript
function is_valid_packet(fields) {

    // test for existing metrics type
    if (fields[1] === undefined) {
        return false;
    }

    // filter out malformed sample rates
    if(fields[2] !== undefined) {
        if(!isValidSampleRate(fields[2])) {
            return false;
        }
    }

    // filter out invalid metrics values
    switch(fields[1]) {
        case 's':
            return true;
        case 'g':
            return isNumber(fields[0]);
        case 'ms':
            return isNumber(fields[0]) && Number(fields[0]) >= 0;
        default:
            if (!isNumber(fields[0])) {
                return false;
            }
            return true;
    }

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.statsd.helpers.writeConfig"></a>[function <span class="apidocSignatureSpan">statsd.helpers.</span>writeConfig (config, stream)](#apidoc.element.statsd.helpers.writeConfig)
- description and source-code
```javascript
writeConfig = function (config, stream) {
  stream.write("\n");
  for (var prop in config) {
    if (!config.hasOwnProperty(prop)) {
      continue;
    }
    if (typeof config[prop] !== 'object') {
      stream.write(prop + ": " + config[prop] + "\n");
      continue;
    }
    var subconfig = config[prop];
    for (var subprop in subconfig) {
      if (!subconfig.hasOwnProperty(subprop)) {
        continue;
      }
      stream.write(prop + " > " + subprop + ": " + subconfig[subprop] + "\n");
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.statsd.logger"></a>[module statsd.logger](#apidoc.module.statsd.logger)

#### <a name="apidoc.element.statsd.logger.Logger"></a>[function <span class="apidocSignatureSpan">statsd.logger.</span>Logger (config)](#apidoc.element.statsd.logger.Logger)
- description and source-code
```javascript
Logger = function (config) {
  this.config  = config;
  this.backend = this.config.backend || 'stdout';
  this.level   = this.config.level || "LOG_INFO";
  if (this.backend == 'stdout') {
    this.util = require('util');
  } else {
    if (this.backend == 'syslog') {
      this.util = require('modern-syslog');
      this.util.init(config.application || 'statsd', this.util.LOG_PID | this.util.LOG_ODELAY, this.util.LOG_LOCAL0);
    } else {
      throw "Logger: Should be 'stdout' or 'syslog'.";
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.statsd.mgmt_console"></a>[module statsd.mgmt_console](#apidoc.module.statsd.mgmt_console)

#### <a name="apidoc.element.statsd.mgmt_console.delete_stats"></a>[function <span class="apidocSignatureSpan">statsd.mgmt_console.</span>delete_stats (stats_type, cmdline, stream)](#apidoc.element.statsd.mgmt_console.delete_stats)
- description and source-code
```javascript
delete_stats = function (stats_type, cmdline, stream) {

  //for each metric requested on the command line
  for (var index in cmdline) {

    //get a list of deletable metrics that match the request
    deletable = existing_stats(stats_type, cmdline[index]);

    //warn if no matches
    if (deletable.length === 0) {
      stream.write("metric " + cmdline[index] + " not found\n");
    }

    //delete all requested metrics
    for (var del_idx in deletable) {
      delete stats_type[deletable[del_idx]];
      stream.write("deleted: " + deletable[del_idx] + "\n");
    }
  }
  stream.write("END\n\n");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.statsd.mgmt_console.existing_stats"></a>[function <span class="apidocSignatureSpan">statsd.mgmt_console.</span>existing_stats (stats_type, bucket)](#apidoc.element.statsd.mgmt_console.existing_stats)
- description and source-code
```javascript
function existing_stats(stats_type, bucket){
  matches = [];

  //typical case: one-off, fully qualified
  if (bucket in stats_type) {
    matches.push(bucket);
  }

  //special case: match a whole 'folder' (and subfolders) of stats
  if (bucket.slice(-2) == ".*") {
    var folder = bucket.slice(0,-1);

    for (var name in stats_type) {
      //check if stat is in bucket, ie~ name starts with folder
      if (name.substring(0, folder.length) == folder) {
        matches.push(name);
      }
    }
  }

  return matches;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.statsd.mgmt_server"></a>[module statsd.mgmt_server](#apidoc.module.statsd.mgmt_server)

#### <a name="apidoc.element.statsd.mgmt_server.start"></a>[function <span class="apidocSignatureSpan">statsd.mgmt_server.</span>start (config, on_data_callback, on_error_callback)](#apidoc.element.statsd.mgmt_server.start)
- description and source-code
```javascript
start = function (config, on_data_callback, on_error_callback) {
  var server = net.createServer(function(stream) {
      stream.setEncoding('ascii');

      stream.on('data', function(data) {
        var cmdline = data.trim().split(" ");
        var cmd = cmdline.shift();

        on_data_callback(cmd, cmdline, stream);
      });

      stream.on('error', function(err) {
        on_error_callback(err, stream);
      });
  });

  server.listen(config.mgmt_port || 8126, config.mgmt_address || undefined);

  return true;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.statsd.process_metrics"></a>[module statsd.process_metrics](#apidoc.module.statsd.process_metrics)

#### <a name="apidoc.element.statsd.process_metrics.process_metrics"></a>[function <span class="apidocSignatureSpan">statsd.</span>process_metrics (metrics, flushInterval, ts, flushCallback)](#apidoc.element.statsd.process_metrics.process_metrics)
- description and source-code
```javascript
process_metrics = function (metrics, flushInterval, ts, flushCallback) {
  var starttime = Date.now();
  var key;
  var counter_rates = {};
  var timer_data = {};
  var statsd_metrics = {};
  var counters = metrics.counters;
  var timers = metrics.timers;
  var timer_counters = metrics.timer_counters;
  var pctThreshold = metrics.pctThreshold;
  var histogram = metrics.histogram;

  for (key in counters) {
    var value = counters[key];

    // calculate "per second" rate
    counter_rates[key] = value / (flushInterval / 1000);
  }

  for (key in timers) {
    var current_timer_data = {};

    if (timers[key].length > 0) {
      timer_data[key] = {};

      var values = timers[key].sort(function (a,b) { return a-b; });
      var count = values.length;
      var min = values[0];
      var max = values[count - 1];

      var cumulativeValues = [min];
      var cumulSumSquaresValues = [min * min];
      for (var i = 1; i < count; i++) {
          cumulativeValues.push(values[i] + cumulativeValues[i-1]);
          cumulSumSquaresValues.push((values[i] * values[i]) +
                                     cumulSumSquaresValues[i - 1]);
      }

      var sum = min;
      var sumSquares = min * min;
      var mean = min;
      var thresholdBoundary = max;

      var key2;

      for (key2 in pctThreshold) {
        var pct = pctThreshold[key2];
        var numInThreshold = count;

        if (count > 1) {
          numInThreshold = Math.round(Math.abs(pct) / 100 * count);
          if (numInThreshold === 0) {
            continue;
          }

          if (pct > 0) {
            thresholdBoundary = values[numInThreshold - 1];
            sum = cumulativeValues[numInThreshold - 1];
            sumSquares = cumulSumSquaresValues[numInThreshold - 1];
          } else {
            thresholdBoundary = values[count - numInThreshold];
            sum = cumulativeValues[count - 1] - cumulativeValues[count - numInThreshold - 1];
            sumSquares = cumulSumSquaresValues[count - 1] -
              cumulSumSquaresValues[count - numInThreshold - 1];
          }
          mean = sum / numInThreshold;
        }

        var clean_pct = '' + pct;
        clean_pct = clean_pct.replace('.', '_').replace('-', 'top');
        current_timer_data["count_" + clean_pct] = numInThreshold;
        current_timer_data["mean_" + clean_pct] = mean;
        current_timer_data[(pct > 0 ? "upper_" : "lower_") + clean_pct] = thresholdBoundary;
        current_timer_data["sum_" + clean_pct] = sum;
        current_timer_data["sum_squares_" + clean_pct] = sumSquares;

      }

      sum = cumulativeValues[count-1];
      sumSquares = cumulSumSquaresValues[count-1];
      mean = sum / count;

      var sumOfDiffs = 0;
      for (var i = 0; i < count; i++) {
         sumOfDiffs += (values[i] - mean) * (values[i] - mean);
      }

      var mid = Math.floor(count/2);
      var median = (count % 2) ? values[mid] : (values[mid-1] + values[mid])/2;

      var stddev = Math.sqrt(sumOfDiffs / count);
      current_timer_data["std"] = stddev;
      current_timer_data["upper"] = max;
      current_timer_data["lower"] = min;
      current_timer_data["count"] = timer_counters[key];
      current_timer_data["count_ps"] = timer_counters[key] / (flushInterval / 1000);
      current_timer_data["sum"] = sum;
      current_timer_data["sum_squares"] = sumSquares;
      current_timer_data["mean"] = mean;
      current_timer_data["median"] = median;

      // note: values bigger than the upper limit of the last bin are ignored, by design
      conf = histogram || [];
      bins = [];
      for (var i = 0; i < conf.length; i++) {
          if (key.indexOf(conf[i].metric) > -1) {
              bins = conf[i].bins;
              break;
          }
      }
      if(bins.length) {
          current_timer_data['histogram'] = {};
      }
      // the outer loop iterates bins, the inner loop iterates timer values;
      // within each run of the inner loop we should only consider the timer value range that's within the scope of the current
bin
      // so we leverage the fact that the values are alread ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.statsd.process_mgmt"></a>[module statsd.process_mgmt](#apidoc.module.statsd.process_mgmt)

#### <a name="apidoc.element.statsd.process_mgmt.init"></a>[function <span class="apidocSignatureSpan">statsd.process_mgmt.</span>init (config)](#apidoc.element.statsd.process_mgmt.init)
- description and source-code
```javascript
init = function (config) {
  conf = config;
  exports.set_title(config);

  process.on('SIGTERM', function() {
   if (conf.debug) {
     util.log('Starting Final Flush');
   }
   healthStatus = 'down';
   process.exit();
  });

}
```
- example usage
```shell
...
  this.backend = this.config.backend || 'stdout';
  this.level   = this.config.level || "LOG_INFO";
  if (this.backend == 'stdout') {
    this.util = require('util');
  } else {
    if (this.backend == 'syslog') {
      this.util = require('modern-syslog');
      this.util.init(config.application || 'statsd', this.util.LOG_PID | this.util.LOG_ODELAY, this.util.LOG_LOCAL0);
    } else {
      throw "Logger: Should be 'stdout' or 'syslog'.";
    }
  }
};

Logger.prototype = {
...
```

#### <a name="apidoc.element.statsd.process_mgmt.set_title"></a>[function <span class="apidocSignatureSpan">statsd.process_mgmt.</span>set_title (config)](#apidoc.element.statsd.process_mgmt.set_title)
- description and source-code
```javascript
set_title = function (config) {
 if (config.title !== undefined) {
   if (config.title) {
       process.title = config.title;
   }
 } else {
   // Respect command line arguments when overriding the process title.
   cmdline = process.argv.slice(2);
   cmdline.unshift('statsd');

   process.title = cmdline.join(" ");
 }
}
```
- example usage
```shell
...

var util = require('util');

var conf;

exports.init = function(config) {
conf = config;
exports.set_title(config);

process.on('SIGTERM', function() {
 if (conf.debug) {
   util.log('Starting Final Flush');
 }
 healthStatus = 'down';
 process.exit();
...
```



# <a name="apidoc.module.statsd.repeater"></a>[module statsd.repeater](#apidoc.module.statsd.repeater)

#### <a name="apidoc.element.statsd.repeater.init"></a>[function <span class="apidocSignatureSpan">statsd.repeater.</span>init (startupTime, config, emitter, logger)](#apidoc.element.statsd.repeater.init)
- description and source-code
```javascript
init = function (startupTime, config, emitter, logger) {
  debug = config.debug;
  l = logger;

  var proto = config.repeaterProtocol;
  if(proto == 'tcp') {
    instance = new TCPRepeaterBackend(startupTime, config, emitter);
  } else {
    instance = new UDPRepeaterBackend(startupTime, config, emitter);
  }

  return true;
}
```
- example usage
```shell
...
  this.backend = this.config.backend || 'stdout';
  this.level   = this.config.level || "LOG_INFO";
  if (this.backend == 'stdout') {
    this.util = require('util');
  } else {
    if (this.backend == 'syslog') {
      this.util = require('modern-syslog');
      this.util.init(config.application || 'statsd', this.util.LOG_PID | this.util.LOG_ODELAY, this.util.LOG_LOCAL0);
    } else {
      throw "Logger: Should be 'stdout' or 'syslog'.";
    }
  }
};

Logger.prototype = {
...
```

#### <a name="apidoc.element.statsd.repeater.stop"></a>[function <span class="apidocSignatureSpan">statsd.repeater.</span>stop (cb)](#apidoc.element.statsd.repeater.stop)
- description and source-code
```javascript
stop = function (cb) {
  if(instance) {
    instance.stop(cb);
    instance = null;
  }
}
```
- example usage
```shell
...

  return true;
};


exports.stop = function(cb) {
  if(instance) {
    instance.stop(cb);
    instance = null;
  }
};
...
```



# <a name="apidoc.module.statsd.set"></a>[module statsd.set](#apidoc.module.statsd.set)

#### <a name="apidoc.element.statsd.set.Set"></a>[function <span class="apidocSignatureSpan">statsd.set.</span>Set ()](#apidoc.element.statsd.set.Set)
- description and source-code
```javascript
Set = function () {
  this.store = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.statsd.tcp"></a>[module statsd.tcp](#apidoc.module.statsd.tcp)

#### <a name="apidoc.element.statsd.tcp.start"></a>[function <span class="apidocSignatureSpan">statsd.tcp.</span>start (config, callback)](#apidoc.element.statsd.tcp.start)
- description and source-code
```javascript
start = function (config, callback) {
  var server = net.createServer(function(stream) {
      stream.setEncoding('ascii');

      var buffer = '';
      stream.on('data', function(data) {
          buffer += data;
          var offset = buffer.lastIndexOf("\n");
          if (offset > -1) {
             var packet = buffer.slice(0, offset + 1);
             buffer = buffer.slice(offset + 1);
             callback(packet, new rinfo(stream, packet));
          }
      });
  });

  server.on('listening', function() {
    config.socket && config.socket_mod && fs.chmod(config.socket, config.socket_mod);
  });

  process.on('exit', function() {
      config.socket && fs.unlinkSync(config.socket);
  });

  server.listen(config.socket || config.port || 8125, config.address || undefined);
  this.server = server;
  return true;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.statsd.udp"></a>[module statsd.udp](#apidoc.module.statsd.udp)

#### <a name="apidoc.element.statsd.udp.start"></a>[function <span class="apidocSignatureSpan">statsd.udp.</span>start (config, callback)](#apidoc.element.statsd.udp.start)
- description and source-code
```javascript
start = function (config, callback) {
  var udp_version = config.address_ipv6 ? 'udp6' : 'udp4';
  var server = dgram.createSocket(udp_version, callback);

  server.bind(config.port || 8125, config.address || undefined);
  this.server = server;

  return true;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
