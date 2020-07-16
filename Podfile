# Pods for Jotify
platform :ios, '13.0'

target 'Jotify' do
  use_frameworks!
  
  # Used in WriteNoteView.swift to create a UITextView with a placeholder
  pod'MultilineTextField'

  # CollectionView layout for SavedNoteController.swift
  # Ignore warnings from Blueprints
  pod'Blueprints', :inhibit_warnings => true

  # Used to animate cells in CollectionView on sort
  pod'ViewAnimator'

  # Used for ActionSheet in SavedNoteController.swift
  pod'XLActionController'
  pod'XLActionController/Skype'

  # Used for picking a static color for notes
  pod'ChromaColorPicker'

  # Fantastic framework for customizing height of presenting viewcontrollers
  # Preferred the setup of 0.5.5, so not updated
  pod'BottomPopup', '~> 0.5.5'

  # Used for displaying confirmations to users when reminders are created or deleted
  pod'SPAlert'

  # Used for verifying purchase receipts for users who bought Jotify as a paid application
  pod'OpenSSL-Universal'
  
  # Used to handle supported device architecture
  post_install do |installer|
      installer.pods_project.targets.each do |target|
          target.build_configurations.each do |config|
              config.build_settings['DEBUG_INFORMATION_FORMAT'] = 'dwarf'
          end
      end
  end

end
