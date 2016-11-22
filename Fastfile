default_platform :iOS

platform :iOS do
  desc "Build iOS"
  lane :build do
    gym(
      archive_path: "./archive",
      output_directory: "./build",
      output_name: "app_name.ipa",
      silent: true,
      export_method: "development",
      disable_xcpretty: true
    )
    crashlytics(
      crashlytics_path: 'Crashlytics.framework',
      api_token: 'your crashlytics api_token',
      build_secret: 'your crashlytics build_secret',
      ipa_path: './build/app_name.ipa',
      notes: 'New build version for iOS release by build machine’
    )
  end
end