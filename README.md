# kanggo-qa-test

import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import static com.kms.katalon.core.testobject.ObjectRepository.findWindowsObject
import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
import com.kms.katalon.core.cucumber.keyword.CucumberBuiltinKeywords as CucumberKW
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import com.kms.katalon.core.model.FailureHandling as FailureHandling
import com.kms.katalon.core.testcase.TestCase as TestCase
import com.kms.katalon.core.testdata.TestData as TestData
import com.kms.katalon.core.testng.keyword.TestNGBuiltinKeywords as TestNGKW
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import com.kms.katalon.core.windows.keyword.WindowsBuiltinKeywords as Windows
import internal.GlobalVariable as GlobalVariable
import org.openqa.selenium.Keys as Keys

//inisiasi url
String url = 'https://www.kanggo.id/'

WebUI.openBrowser(url) //open browser dengan variable url yang telah diinisiasi
WebUI.maximizeWindow() //menampilkan full window pada browser
WebUI.click(findTestObject('Object Repository/Page_Jasa Tukang Bangunan  Aplikasi Pertukangan No 1  Kanggo/button_Perbaiki Bangunan')) //klik button perbaiki bangunan
WebUI.click(findTestObject('Object Repository/Page_Jasa Tukang Bangunan  Aplikasi Pertukangan No 1  Kanggo/dropdown_Untuk Perusahaan')) //pilih menu dropdown untuk perusahaan
WebUI.verifyElementPresent(findTestObject('Object Repository/Page_Jasa Perbaikan dan Pemelihara Bangunan untuk Perusahaan  Kanggo/Kelola Bangunan Bisnis dengan Nyaman Bersama Kanggo'), 0, FailureHandling.STOP_ON_FAILURE) //verify if user bisa mengakses halaman https://www.kanggo.id/untuk-perusahaan ditandai dengan munculnya text "Kelola Bangunan Bisnis dengan Nyaman Bersama Kanggo"
WebUI.closeBrowser() //tutup browser
