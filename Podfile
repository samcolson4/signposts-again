# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

target 'signposts-again' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!

  # Pods for signposts-again
  pod 'Firebase/Auth'
  pod 'Firebase/Firestore'
  pod 'FirebaseFirestoreSwift'
  pod 'Firebase/Auth'
  pod 'Firebase/Storage'
  pod 'Kingfisher'

  target 'signposts-againTests' do
    inherit! :search_paths
    # Pods for testing
  end

  target 'signposts-againUITests' do
    # Pods for testing
  end
  
  post_install do |pi|
     t = pi.pods_project.targets.find { |t| t.name == 'Firebase' }
     t.build_configurations.each do |bc|
       bc.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '9.0'
     end
  end

end
