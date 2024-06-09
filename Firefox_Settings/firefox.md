This is a collection of privacy improving settings to manually enter into 
the Firefox `about:config` webpage. While this normally is added as a 
user.js file, a Flatpak install of Firefox doesn't allow this to work.Each section is broken down into catagories that the setting applies to.

_Either make a backup of your current profile or create a new profile before
applying these settings as they can create issues._
***************************************************************************

### ENABLE TRACKING PROTECTION
- browser.contentblocking.category: "strict"
- network.cookie.sameSite.noneRequiresSecure: true
- browser.helperApps.deleteTempFileOnExit: true
- privacy.globalprivacycontrol.enabled: true

### MODIFY URL BAR DEFAULTS
- browser.urlbar.suggest.quicksuggest.sponsored: false
- browser.urlbar.suggest.quicksuggest.nonsponsored: false
- browser.formfill.enable: false
- security.insecure_connection_text.enabled: true
- security.insecure_connection_text.pbmode.enabled: true
- network.IDN_show_punycode: true
- browser.urlbar.suggest.calculator: true
- browser.urlbar.unitConversion.enabled: true
- browser.urlbar.trending.featureGate: false

### IMPROVE MIXED CONTENT & CROSS-SITE SCRIPTING
- security.mixed_content.block_display_content: true
- security.mixed_content.upgrade_display_content: true
- security.mixed_content.upgrade_display_content.image: true
- pdfjs.enableScripting: false
- extensions.postDownloadThirdPartyPrompt: false
- network.http.referer.XOriginTrimmingPolicy: 2

### ENABLE WEBRTC BEHIND PROXY
- media.peerconnection.ice.proxy_only_if_behind_proxy: true
- media.peerconnection.ice.default_address_only: true

### NETWORK SETTINGS
- network.http.max-connections: 1800
- network.http.max-persistent-connections-per-server: 10
- network.http.max-urgent-start-excessive-connections-per-host: 5
- network.http.pacing.requests.enabled: false
- network.dnsCacheExpiration: 3600
- network.ssl_tokens_cache_capacity: 10240
- security.ssl.treat_unsafe_negotiation_as_broken: true
- browser.xul.error_pages.expert_bad_cert: true
- security.tls.enable_0rtt_data: false
- security.OCSP.enabled: 0
- security.remote_settings.crlite_filters.enabled: true
- security.pki.crlite_mode: 2
- dom.security.https_only_mode: true
- dom.security.https_only_mode_error_page_user_suggestions: true
- dom.security.https_first: true
- dom.security.https_first_schemeless: true

### SPECULATIVE LOADING
- network.dns.disablePrefetch: true
- network.dns.disablePrefetchFromHTTPS: true
- network.prefetch-next: false
- network.predictor.enabled: false
- network.predictor.enable-prefetch: false

### DIABLE BUILT-IN PASSWORDS
- signon.formlessCapture.enabled: false
- signon.privateBrowsingCapture.enabled: false
- network.auth.subresource-http-auth-allow: 1
- editor.truncate_user_pastes: false

### DISABLE TELEMETRY
- datareporting.policy.dataSubmissionEnabled: false
- datareporting.healthreport.uploadEnabled: false
- toolkit.telemetry.unified: false
- toolkit.telemetry.enabled: false
- toolkit.telemetry.server: "data:,"
- toolkit.telemetry.archive.enabled: false
- toolkit.telemetry.newProfilePing.enabled: false
- toolkit.telemetry.shutdownPingSender.enabled: false
- toolkit.telemetry.updatePing.enabled: false
- toolkit.telemetry.bhrPing.enabled: false
- toolkit.telemetry.firstShutdownPing.enabled: false
- toolkit.telemetry.coverage.opt-out: true
- toolkit.coverage.opt-out: true
- toolkit.coverage.endpoint.base: ""
- browser.newtabpage.activity-stream.feeds.telemetry: false
- browser.newtabpage.activity-stream.telemetry: false

### DISABLE EXPERIMENTS
- app.shield.optoutstudies.enabled: false
- app.normandy.enabled: false
- app.normandy.api_url: ""

### DON'T SEND CRASH REPORTS
- breakpad.reportURL: ""
- browser.tabs.crashReporting.sendReport: false
- browser.crashReports.unsubmittedCheck.autoSubmit2: false

### DEFAULT MOZILLA CHANGES
- browser.privatebrowsing.vpnpromourl: ""
- extensions.getAddons.showPane: false
- extensions.htmlaboutaddons.recommendations.enabled: false
- browser.discovery.enabled: false
- browser.shell.checkDefaultBrowser: false
- browser.newtabpage.activity-stream.asrouter.userprefs.cfr.addons: false
- browser.newtabpage.activity-stream.asrouter.userprefs.cfr.features: false
- browser.preferences.moreFromMozilla: false
- browser.tabs.tabmanager.enabled: false
- browser.aboutConfig.showWarning: false
- browser.aboutwelcome.enabled: false
- browser.newtabpage.activity-stream.feeds.topsites: false
- browser.newtabpage.activity-stream.feeds.section.topstories: false
- extensions.pocket.enabled: false
- browser.download.open_pdf_attachments_inline: true
- signon.rememberSignons: false
- extensions.formautofill.addresses.enabled: false
- extensions.formautofill.creditCards.enabled: false
- cookiebanners.service.mode: 1
- cookiebanners.service.mode.privateBrowsing: 1
- permissions.default.desktop-notification: 2
- permissions.default.geo: 2
- geo.provider.network.url: "https://location.services.mozilla.com/v1/geolocate?key=%MOZILLA_API_KEY%"
- permissions.manager.defaultsUrl: ""
- webchannel.allowObject.urlWhitelist: ""