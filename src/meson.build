appcenter_files = files(
    'Application.vala',
    'AsyncMutex.vala',
    'MainWindow.vala',
    'SuspendControl.vala',
    'Utils.vala',
    'Core/BackendAggregator.vala',
    'Core/BackendInterface.vala',
    'Core/ChangeInformation.vala',
    'Core/Client.vala',
    'Core/ComponentValidator.vala',
    'Core/FlatpakBackend.vala',
    'Core/Houston.vala',
    'Core/Job.vala',
    'Core/Package.vala',
    'Core/PackageKitBackend.vala',
    'Core/ScreenshotCache.vala',
    'Core/Task.vala',
    'Core/UbuntuDriversBackend.vala',
    'Core/UpdateManager.vala',
    'Dialogs/ContentWarningDialog.vala',
    'Dialogs/InstallFailDialog.vala',
    'Dialogs/NonCuratedWarningDialog.vala',
    'Dialogs/RestartDialog.vala',
    'Dialogs/StripeDialog.vala',
    'Dialogs/UninstallConfirmDialog.vala',
    'Dialogs/UninstallFailDialog.vala',
    'Dialogs/UpdateFailDialog.vala',
    'Services/DBusInterfaces.vala',
    'Services/DBusServer.vala',
    'Services/SearchProvider.vala',
    'Views/AppInfoView.vala',
    'Views/AppListUpdateView.vala',
    'Views/AppListView.vala',
    'Views/Homepage.vala',
    'Views/InstalledView.vala',
    'Views/SearchView.vala',
    'Views/AbstractView.vala',
    'Widgets/AbstractAppList.vala',
    'Widgets/AppListRow.vala',
    'Widgets/Banner.vala',
    'Widgets/CardNumberEntry.vala',
    'Widgets/CategoryFlowBox.vala',
    'Widgets/CategoryItem.vala',
    'Widgets/HumbleButton.vala',
    'Widgets/HumblePopover.vala',
    'Widgets/NetworkInfoBar.vala',
    'Widgets/PackageRow.vala',
    'Widgets/ReleaseListBox.vala',
    'Widgets/ReleaseRow.vala',
    'Widgets/SharePopover.vala',
    'Widgets/SizeLabel.vala',
    'Widgets/Switcher.vala',
    'Widgets/UpdateHeaderRow.vala',
    'Widgets/AppContainers/AbstractAppContainer.vala',
    'Widgets/AppContainers/AbstractPackageRowGrid.vala',
    'Widgets/AppContainers/InstalledPackageRowGrid.vala',
    'Widgets/AppContainers/ListPackageRowGrid.vala',
    'Widgets/Carousel/AuthorCarousel.vala',
    'Widgets/Carousel/Carousel.vala',
    'Widgets/Carousel/CarouselItem.vala'
)

config_file = configure_file(
    input: 'config.vala.in',
    output: 'config.vala',
    configuration: conf_data
)

args = []
if get_option('curated')
    args += '--define=CURATED'
endif

if get_option('homepage')
    args += '--define=HOMEPAGE'
endif

if get_option('payments')
    args += '--define=PAYMENTS'
endif

if get_option('sharing')
    args += '--define=SHARING'
endif

executable(
    meson.project_name(),
    appcenter_files,
    config_file,
    css_gresource,
    icons_gresource,
    dependencies: dependencies,
    vala_args: args,
    install: true
)
