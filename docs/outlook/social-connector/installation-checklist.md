---
title: Checkliste für Installation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: In diesem Thema werden die Voraussetzungen für die erfolgreiche Installation eines OSC-Anbieters (Outlook Connector für soziale Netzwerke) beschrieben, und bei der Installation wird überprüft, ob das Installationsprogramm des Anbieters abgeschlossen sein sollte, damit es ordnungsgemäß funktioniert.
ms.openlocfilehash: aaed852edd9a3f4e30ec5fdcc4afbdd32eed0442
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560403"
---
# <a name="installation-checklist"></a>Checkliste für Installation

In diesem Thema werden die Voraussetzungen für die erfolgreiche Installation eines OSC-Anbieters (Outlook Connector für soziale Netzwerke) beschrieben, und bei der Installation wird überprüft, ob das Installationsprogramm des Anbieters abgeschlossen sein sollte, damit es ordnungsgemäß funktioniert.
  
## <a name="installation-overview"></a>Übersicht über die Installation

Benutzer sollten OSC-Anbieter nur installieren, wenn eine unterstützende Version von Outlook vorhanden ist und osc auf dem Clientcomputer installiert und aktiviert ist. Unterstützende Versionen von Outlook sind Office Outlook 2003, Office Outlook 2007, Outlook 2010 und Outlook 2013 (installiert auf dem Clientcomputer oder im Fall von Outlook 2010 und Outlook 2013, bereitgestellt von Klick-und-Los auf dem Clientcomputer). Um eine erfolgreiche Installation sicherzustellen, sollte das Anbieterinstallationsprogramm Folgendes ausführen:
  
- Überprüfen Sie, ob eine unterstützte Version von Outlook vorhanden ist.
    
- Überprüfen Sie, ob osc installiert ist.
    
> [!NOTE]
> Klick-und-Los ist eine virtuelle Umgebung, in der Outlook 2010 (32-Bit) oder Outlook 2013 (32-Bit) ausgeführt werden kann. Überprüfen Sie für Outlook 2013, ob der Schlüssel "VirtualOutlook" in HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook der Windows-Registrierung vorhanden ist. Weitere Informationen zur Bereitstellung von Outlook als Klick-und-Los-Produkt auf einem Clientcomputer finden Sie unter ["Überprüfen, ob Outlook auf einem Computer als Klick-und-Los-Produkt verfügbar ist".](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx) 
  
Der Benutzer muss jedoch sicherstellen, dass osc aktiviert ist, bevor er den Anbieter installiert.
  
Drittanbieter, einschließlich OSC-Anbieter, können das OSC nicht weitervertren. Wenn das OSC jedoch nicht installiert ist, kann das Anbieter-Installationsprogramm die entsprechenden g-Links verwenden, um osc auf dem Clientcomputer zu installieren. Ein g-Link ist eine speziell erstellte https://g.live.com URL, die einen Benutzer an eine entsprechende Webseite weiterleitet, um den OSC herunterzuladen. Eine OSC-G-Verknüpfung ist als https://g.live.com/0CR _LCID_ /  _Glink_ formatiert, wobei _LCID_ und _Glink_ das Gebietsschema, die Version und die Bitanzahl der Outlook auf dem Clientcomputer angeben. Jeder g-Link verweist auf eine ausführbare Datei und ist spezifisch für die angegebenen _LCID-_ und _Glink-Werte._ 
  
Beispielsweise lautet der g-Link zum Installieren der neuesten Version von OSC für Outlook 2003 oder Outlook 2007 für die LCID 1033 (Englisch (USA) wie folgt:
  
https://g.live.com/0CR1033/80
  
Ausführliche Informationen zu _Glink-Werten_ für unterschiedliche Versionen und Bitanzahl von Outlook und _LCID-Werten_ für unterstützte Gebietsschemas finden Sie unter #7 im Abschnitt [Installation Checklist](#olosc_InstallationOverview_InstallationChecklist) below. 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>Checkliste für Installation

Das Anbietereinrichtungspaket sollte eine Reihe von Installationsüberprüfungen durchführen, wie in Abbildung 1 dargestellt, um sicherzustellen, dass der Anbieter erfolgreich installiert wird.
  
**Abbildung 1. Anbieterinstallationslogik**

![Checkliste für Installation](media/odc_ol14_ta_OSC_Fig07.gif)
  
Im folgenden Verfahren werden die in Abbildung 1 beschriebenen Installationsüberprüfungen beschrieben.
  
1. Ermitteln Sie als Voraussetzung, ob Outlook installiert oder vorhanden ist, und ermitteln Sie, ob die Version von Outlook OSC unterstützt. Weitere Informationen zum Erkennen der installierten Version von Outlook finden Sie unter ["Überprüfen der Version von Outlook".](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx)
    
   - Wenn die installierte Version von Outlook älter als Outlook 2003 ist, kann der Installationsvorgang des Anbieters nicht abgeschlossen werden. Informieren Sie den Benutzer, eine unterstützte Version von Outlook und osc abzurufen, bevor Sie mit der Installation des OSC-Anbieters fortfahren.
    
   - Wenn Outlook nicht installiert ist, fahren Sie mit Schritt 2 fort.
    
   - Wenn Outlook 2003 oder Outlook 2007 installiert ist, fahren Sie mit Schritt 3 fort. 
    
   - Wenn Outlook 2010 oder Outlook 2013 installiert ist, fahren Sie mit Schritt 4 fort.
    
2. **Fahren Sie mit diesem Schritt fort, wenn Outlook nicht auf dem Clientcomputer installiert ist:**
    
   1. Überprüfen Sie, ob osc als Standardkomponente einer Klick-und-Los-Installation von Outlook 2010 oder Outlook 2013 installiert ist. Überprüfen Sie den `VirtualOutlook` Schlüssel am folgenden Speicherort in der Windows-Registrierung: 
      
      - For Outlook 2010,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - For Outlook Social Connector 2013,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      Der  `VirtualOutlook` Schlüssel ist ein REG_SZ Wert, der das Gebietsschematag wie "en-us" des installierten Produkts enthält. 
      
   2. Wenn der `VirtualOutlook` Schlüssel nicht vorhanden ist, ist Outlook nicht auf dem Clientcomputer vorhanden, und die Installation des Anbieters kann nicht abgeschlossen werden. Informieren Sie den Benutzer, eine unterstützte Version von Outlook und osc abzurufen, bevor Sie mit der Installation des OSC-Anbieters fortfahren. 
      
   3. Wenn der `VirtualOutlook` Schlüssel vorhanden ist, wurde Outlook per Klick-und-Los auf dem Clientcomputer übermittelt. Überprüfen Sie die installierte Version der OSC-Typbibliothek, indem Sie den `OSCVersion` Schlüssel am folgenden Speicherort in der Windows Registrierung untersuchen: 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      Der Wert von  `OSCVersion` ist eine Zeichenfolge, die die Versionsnummer der Typbibliothek von Socialprovider.dll angibt (z. B. "1.0", "1.1" oder "15"). 
      
   4. Wenn  `OSCVersion` "1.0", "1.1" oder "15" ist, wird eine entsprechende Version von OSC installiert. Fahren Sie mit Schritt 6 fort, um das aktuelle Outlook Gebietsschema der Benutzeroberfläche zu finden, um sich auf die Installation der neuesten Version von OSC vorzubereiten. 
      
   5. Enthält andernfalls  `OSCVersion` keinen erwarteten Wert. Fahren Sie mit Schritt 6 fort, um das aktuelle Outlook Gebietsschema der Benutzeroberfläche zu finden, um sich auf die Installation einer geeigneten Version von OSC vorzubereiten. 
    
3. **Fahren Sie mit diesem Schritt fort, wenn Outlook 2003 oder Outlook 2007 auf dem Clientcomputer installiert ist:**
    
   1. Überprüfen Sie, ob osc installiert ist, indem Sie eine benutzerdefinierte Installer-Aktion schreiben, um das Vorhandensein der folgenden qualifizierten Komponenten-ID zu testen:
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      Die qualifizierte Komponenten-ID ist eine GUID, die eine Methode der Dereferenzierung auf einer Ebene bereitstellt, ähnlich wie ein Zeiger. Weitere Informationen zu Windows Installer finden Sie unter [Roadmap to Windows Installer Documentation](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation).
      
   2. Wenn die angegebene qualifizierte Komponente vorhanden ist, wird eine Version des OSC installiert. Fahren Sie mit Schritt 5 fort, um das aktuelle Outlook Gebietsschema der Benutzeroberfläche zu finden, um sich auf die Installation der neuesten Version von OSC vorzubereiten.
      
   3. Andernfalls wird das OSC nicht installiert. Fahren Sie mit Schritt 6 fort, um das aktuelle Outlook Gebietsschema der Benutzeroberfläche zu finden, um sich auf die Installation einer geeigneten Version von OSC vorzubereiten.
      
4. **Fahren Sie mit diesem Schritt fort, wenn Outlook 2010 oder Outlook 2013 auf dem Clientcomputer installiert ist:**
    
   1. Ermitteln Sie die Bitanzahl der installierten Version von Outlook, indem Sie den `Bitness` Schlüssel am folgenden Speicherort in der Windows Registrierung untersuchen: 
      
      - For Outlook 2010, look at`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - For Outlook 2013, look at`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      Der `Bitness` Schlüssel ist "x86" für 32-Bit-Outlook oder "x64" für 64-Bit-Outlook. 
      
   2. Wenn Ihr Anbieter ein verwalteter Anbieter ist und Sie die Anbieterkomponente kompiliert haben, die die Zielplattform als **beliebige CPU** angibt, fahren Sie mit Schritt 6 fort, um das aktuelle Outlook Gebietsschema der Benutzeroberfläche zu finden, um sich auf die Installation der neuesten Version von OSC vorzubereiten. Ihr Anbieter funktioniert sowohl mit 32-Bit- als auch mit 64-Bit-Versionen des OSC.
      
   3. Wenn Ihr Anbieter eine systemeigene COM-Komponente ist, überprüfen Sie die Bitanzahl der installierten Version von Outlook:
      
      - Wenn die installierte Version von Outlook 32-Bit ist, muss ihr Installationsvorgang einen 32-Bit-Anbieter (in Schritt 8) installieren, nachdem sichergestellt wurde, dass ein entsprechendes OSC installiert ist.
      
      - Andernfalls ist die installierte Version von Outlook 64-Bit, und Ihr Installationsvorgang muss einen 64-Bit-Anbieter (in Schritt 8) installieren, nachdem sichergestellt wurde, dass ein geeigneter OSC installiert ist. 
      
   4. Fahren Sie mit Schritt 6 fort, um das aktuelle Outlook Gebietsschema der Benutzeroberfläche zu finden, um sich auf die Installation einer entsprechenden Version des OSC vorzubereiten.
    
5. **Fahren Sie mit diesem Schritt fort, wenn Outlook 2003 oder Outlook 2007 installiert ist und der OSC auf dem Clientcomputer installiert ist:** Überprüfen Sie das aktuelle Outlook Gebietsschema der Benutzeroberfläche, indem Sie den `OSCLcid` Schlüssel an der folgenden Stelle in der registrierung Windows überprüfen: 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   Der `OSCLcid` Schlüssel ist ein DWORD-Wert, der das IETF-Gebietsschematag (Internet Engineering Task Force) (definiert durch [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) und [[RFC4647] )](https://www.ietf.org/rfc/rfc4647.txt)angibt, das das aktuelle Outlook Gebietsschemas der Benutzeroberfläche darstellt. Fahren Sie mit Schritt 7 fort, um den neuesten OSC auf dem Clientcomputer zu installieren.
    
6. **Fahren Sie mit diesem Schritt fort, wenn Outlook 2003 oder Outlook 2007 installiert ist oder Outlook 2010 oder Outlook 2013 vorhanden ist, der neueste OSC jedoch nicht unbedingt auf dem Clientcomputer installiert ist:**
    
   Verwenden Sie das **LanguageSettings** -Objekt, um die LCID des Outlook Gebietsschemas der Benutzeroberfläche zu bestimmen. Der folgende Codeausschnitt Visual Basic Scripting Edition (VBScript) veranschaulicht, wie Sie die LCID des gebietsschemas der Outlook Benutzeroberfläche abrufen. 
    
   ```vb
    Function GetOutlookUI_LCID()
        ' Declare variables.
        Dim msoLanguageIDUI, olApp
        msoLanguageIDUI = 2
        Set olApp = CreateObject("Outlook.Application")
        ' Return Outlook UI LCID.
        GetOutlookUI_LCID = olApp.LanguageSettings.LanguageID(msoLanguageIDUI)
    End Function
   ```

7. **Fahren Sie mit diesem Schritt fort, wenn das Installationsprogramm über die LCID der installierten Version von Outlook verfügt, der neueste OSC jedoch nicht unbedingt auf dem Clientcomputer installiert ist:**
    
   Verketten Sie eine g-Verknüpfung mit Ihrem Installationspaket, um sicherzustellen, dass die neueste Version des OSC auf dem Clientcomputer installiert ist. Das g-Link-Format lautet wie folgt:
    
   https://g.live.com/0CR_LCID_ /  _Glink_
    
   In Tabelle 1 unten finden Sie die unterstützten _LCID-Werte_ und in Tabelle 2 die unterstützten _Glink-Werte._ Der g-Link zum Installieren der neuesten Version des 32-Bit-OSC für 32-Bit-Outlook Connector für soziale Netzwerke 2013 (ENGLISCH) lautet beispielsweise wie folgt: 
    
   https://g.live.com/0CR1033/82
    
8. Installieren Sie den Anbieter. Das Installationsverfahren des Anbieters muss die Programmkennung (ProgID) im entsprechenden Windows Registrierungsspeicherort registrieren. Weitere Informationen finden Sie unter [Registrieren eines Anbieters.](registering-a-provider.md) Stellen Sie außerdem sicher, dass die Bitanzahl des zu installierenden Anbieters mit der Bitanzahl der Version von Outlook auf dem Clientcomputer identisch ist. Installieren Sie beispielsweise einen 32-Bit-Anbieter, wenn 32-Bit-Outlook 2013 vorhanden ist, und einen 64-Bit-Anbieter, wenn 64-Bit-Outlook 2013 installiert ist. Für Outlook 2003 oder 2007 gilt nur die 32-Bit-Version Ihres Anbieters. 
    
**Tabelle 1: Unterstützte Gebietsschema- und entsprechende LCID-Werte in Hexadezimalwert für osc**
  
|**Locale**|**LCID**|
|:-----|:-----|
|ar-sa  <br/> |1025  <br/> |
|bg-bg  <br/> |1026  <br/> |
|ca-es  <br/> |1027  <br/> |
|cs-cz  <br/> |1029  <br/> |
|da-dk  <br/> |1030  <br/> |
|de-de  <br/> |1031  <br/> |
|el-gr  <br/> |1032  <br/> |
|en-us  <br/> |1033  <br/> |
|es-es  <br/> |3082  <br/> |
|et-ee  <br/> |1061  <br/> |
|eu-es  <br/> |1069  <br/> |
|fi-fi  <br/> |1035  <br/> |
|fr-fr  <br/> |1036  <br/> |
|gl-es  <br/> |1110  <br/> |
|he-il  <br/> |1037  <br/> |
|hi-in  <br/> |1081  <br/> |
|hr-hr  <br/> |1050  <br/> |
|hu-hu  <br/> |1038  <br/> |
|it-it  <br/> |1040  <br/> |
|ja-jp  <br/> |1041  <br/> |
|kk-kz  <br/> |1087  <br/> |
|ko-kr  <br/> |1042  <br/> |
|lt-lt  <br/> |1063  <br/> |
|lv-lv  <br/> |1062  <br/> |
|nb-no  <br/> |1044  <br/> |
|nl-nl  <br/> |1043  <br/> |
|pl-pl  <br/> |1045  <br/> |
|pt-br  <br/> |1046  <br/> |
|pt-pt  <br/> |2070  <br/> |
|ro-ro  <br/> |1048  <br/> |
|ru-ru  <br/> |1049  <br/> |
|sk-sk  <br/> |1051  <br/> |
|sl-si  <br/> |1060  <br/> |
|sr-cyrl-cs  <br/> |3098  <br/> |
|sr-latn-cs  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |
   
**Tabelle 2: Unterstützte Glink-Werte für osc**
  
|**Glink-Wert**|**Funktion**|
|:-----|:-----|
|80  <br/> |Installiert die neueste Version von OSC für Outlook 2003 oder Outlook 2007.  <br/> |
|82  <br/> |Installiert den neuesten Patch von 32-Bit-OSC für Outlook 2007, Outlook 2010 oder Outlook Connector für soziale Netzwerke 2013.  <br/> |
|83  <br/> |Installiert den neuesten Patch von 64-Bit-OSC für Outlook 2010 oder Outlook Connector für soziale Netzwerke 2013.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Registrieren eines Anbieters](registering-a-provider.md) 
- [Schnelle Schritte für Learning zum Entwickeln eines Anbieters](quick-steps-for-learning-to-develop-a-provider.md)
- [Bereitstellen eines Providers](deploying-a-provider.md)

