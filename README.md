# Ehis_M
import android.app.Application
import com.maxmind.device.DeviceTracker
import com.maxmind.device.SdkConfig

class MyApplication : Application() {
    override fun onCreate() {
        super.onCreate()

        val config = SdkConfig.Builder(MAXMIND_ACCOUNT_ID).build()
        DeviceTracker.initialize(this, config)
    }
}