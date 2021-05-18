---
title: Checkliste für Installation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: In diesem Thema werden die Voraussetzungen für die erfolgreiche Installation eines Outlook Social Connector (OSC)-Anbieters beschrieben, und die Installation überprüft, ob das Installationsprogramm des Anbieters ordnungsgemäß ausgeführt werden sollte.
ms.openlocfilehash: 8fec8523e57ad2678d02a0c5cbc1ad57340e5267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286340"
---
# <a name="installation-checklist"></a>Checkliste für Installation

In diesem Thema werden die Voraussetzungen für die erfolgreiche Installation eines Outlook Social Connector (OSC)-Anbieters beschrieben, und die Installation überprüft, ob das Installationsprogramm des Anbieters ordnungsgemäß ausgeführt werden sollte.
  
## <a name="installation-overview"></a>Installationsübersicht

Benutzer sollten OSC-Anbieter nur installieren, wenn eine unterstützende Version von Outlook vorhanden ist und das Betriebssystem auf dem Clientcomputer installiert und aktiviert ist. Unterstützende Versionen von Outlook sind Office Outlook 2003, Office Outlook 2007, Outlook 2010 und Outlook 2013 (auf dem Clientcomputer installiert oder im Fall von Outlook 2010 und Outlook 2013 von Klick-und-Ausführen auf dem Clientcomputer). Um eine erfolgreiche Installation zu gewährleisten, sollte Das Installationsprogramm des Anbieters die folgenden Schritte ausführen:
  
- Überprüfen Sie, ob eine unterstützte Outlook vorhanden ist.
    
- Überprüfen Sie, ob das OSC installiert ist.
    
> [!NOTE]
> Click-to-Run ist eine virtuelle Umgebung, in der Outlook 2010 (32-Bit) oder Outlook 2013 (32-Bit) ausgeführt werden kann. Überprüfen Outlook 2013, ob der VirtualOutlook-Schlüssel in der HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook der Windows vorhanden ist. Weitere Informationen zum Bereitstellen von Outlook als Klick-und-Klick-Produkt auf einem Clientcomputer finden Sie unter [How to Verify if Outlook is Available on a Computer as a Click-to-Run Product](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx). 
  
Der Benutzer muss jedoch sicherstellen, dass das Betriebssystem aktiviert ist, bevor er den Anbieter installiert.
  
Drittanbieter, einschließlich OSC-Anbieter, können das OSC nicht weiterverteilen. Wenn das Betriebssystem jedoch nicht installiert ist, kann das Anbieterinstallationsprogramm geeignete g-Links verwenden, um das Betriebssystem auf dem Clientcomputer zu installieren. Ein g-link ist eine speziell konstruierte URL, auf der ein Benutzer an eine entsprechende Webseite weitergeleitet wird, https://g.live.com um das OSC herunterzuladen. Ein OSC g-link ist als https://g.live.com/0CR _LCID_ /  _Glink_ formatiert, wobei _LCID_ und _Glink_ das Locale, version und bitness von Outlook auf dem Clientcomputer angeben. Jeder g-Link verweist auf eine ausführbare Datei und ist spezifisch für die angegebenen _LCID-_ und _Glink-Werte._ 
  
Der g-Link zum Installieren der neuesten Version des Betriebssystems für Outlook 2003 oder Outlook 2007 für die LCID 1033 (US Englisch) lautet beispielsweise wie folgt:
  
https://g.live.com/0CR1033/80
  
Weitere Informationen zu _Glink-Werten_ für unterschiedliche Versionen und bitness von Outlook und _LCID-Werten_ für unterstützte Locales finden Sie #7 im Abschnitt [Installationscheckliste](#olosc_InstallationOverview_InstallationChecklist) weiter unten. 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>Checkliste für Installation

Das Anbietereinrichtungspaket sollte eine Reihe von Installationsüberprüfungen durchführen, wie in Abbildung 1 dargestellt, um sicherzustellen, dass der Anbieter erfolgreich installiert wird.
  
**Abbildung 1. Installationslogik des Anbieters**

![Checkliste für Installation](media/odc_ol14_ta_OSC_Fig07.gif)
  
Im folgenden Verfahren werden die in Abbildung 1 beschriebenen Installationsüberprüfungen beschrieben.
  
1. Ermitteln Sie als Voraussetzung, ob Outlook installiert oder vorhanden ist, und ermitteln Sie, ob die Version von Outlook osC unterstützt wird. Weitere Informationen zum Erkennen der installierten Version von Outlook finden Sie unter [Überprüfen der Version von Outlook](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx).
    
   - Wenn die installierte Version von Outlook vor Outlook 2003 liegt, kann das Installationsprozedur des Anbieters nicht abgeschlossen werden. Informieren Sie den Benutzer, eine unterstützte Version von Outlook osC zu erhalten, bevor Sie mit der Installation des OSC-Anbieters fortfahren.
    
   - Wenn Outlook nicht installiert ist, fahren Sie mit Schritt 2 fort.
    
   - Wenn Outlook 2003 oder Outlook 2007 installiert ist, fahren Sie mit Schritt 3 fort. 
    
   - Wenn Outlook 2010 oder Outlook 2013 installiert ist, fahren Sie mit Schritt 4 fort.
    
2. **Fahren Sie mit diesem Schritt fort, Outlook nicht auf dem Clientcomputer installiert ist:**
    
   1. Überprüfen Sie, ob das Betriebssystem als Standardkomponente einer Klick-und-Aus-Installation von Outlook 2010 oder Outlook 2013 installiert ist. Untersuchen Sie `VirtualOutlook` den Schlüssel am folgenden Speicherort in der Windows Registrierung: 
      
      - Für Outlook 2010`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - For Outlook Social Connector 2013,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      Der Schlüssel ist ein REG_SZ, der das Locale-Tag enthält, z. B.  `VirtualOutlook` "en-us&quot; des installierten Produkts. 
      
   2. Wenn der Schlüssel nicht vorhanden ist, Outlook nicht auf dem Clientcomputer vorhanden ist, und das Installationsverfahren des Anbieters `VirtualOutlook` kann nicht abgeschlossen werden. Informieren Sie den Benutzer, eine unterstützte Version von Outlook osC zu erhalten, bevor Sie mit der Installation des OSC-Anbieters fortfahren. 
      
   3. Wenn der `VirtualOutlook` Schlüssel vorhanden ist, Outlook von Klick-und-Ausführen auf dem Clientcomputer zugestellt. Fahren Sie mit der Überprüfung der installierten Version der OSC-Typbibliothek fort, indem Sie den Schlüssel am folgenden Speicherort in der Windows `OSCVersion` untersuchen: 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      Der Wert von ist eine Zeichenfolge, die die  `OSCVersion` Typbibliotheksversionsnummer von Socialprovider.dll angibt (z. B. &quot;1.0&quot;, &quot;1.1&quot; oder &quot;15"). 
      
   4. Wenn  `OSCVersion` "1.0", "1.1" oder "15" ist, wird eine entsprechende Version von OSC installiert. Fahren Sie mit Schritt 6 fort, um das aktuelle Outlook-Benutzeroberflächen-Locale zu finden, um die Installation der neuesten Version des Betriebssystems vorzubereiten. 
      
   5. Andernfalls  `OSCVersion` enthält keinen erwarteten Wert. Fahren Sie mit Schritt 6 fort, um das aktuelle Outlook zu finden, um die Installation einer geeigneten Version des Betriebssystems vorzubereiten. 
    
3. **Fahren Sie mit diesem Schritt fort, Outlook 2003 oder Outlook 2007 auf dem Clientcomputer installiert ist:**
    
   1. Überprüfen Sie, ob das OSC installiert ist, indem Sie eine benutzerdefinierte Installeraktion schreiben, um das Vorhandensein der folgenden qualifizierten Komponenten-ID zu testen:
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      Bei der qualifizierten Komponenten-ID handelt es sich um eine GUID, die eine Methode der Ein-Ebenen-De indirekten, ähnlich einem Zeiger, bietet. Weitere Informationen zum Installationsprogramm Windows finden Sie unter [Roadmap to Windows Installer Documentation](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation).
      
   2. Wenn die angegebene qualifizierte Komponente vorhanden ist, wird eine Version des Betriebssystems installiert. Fahren Sie mit Schritt 5 fort, um das aktuelle Outlook zu finden, um die Installation der neuesten Version des Betriebssystems vorzubereiten.
      
   3. Andernfalls wird der OSC nicht installiert. Fahren Sie mit Schritt 6 fort, um das aktuelle Outlook zu finden, um die Installation einer geeigneten Version des Betriebssystems vorzubereiten.
      
4. **Fahren Sie mit diesem Schritt fort, Outlook 2010 oder Outlook 2013 auf dem Clientcomputer installiert ist:**
    
   1. Ermitteln Sie die Bitität der installierten Version von Outlook, indem Sie den Schlüssel am folgenden Speicherort in der Windows `Bitness` untersuchen: 
      
      - Weitere Outlook 2010`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - Weitere Outlook 2013`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      Der `Bitness` Schlüssel ist "x86" für 32-Bit-Outlook oder "x64" für 64-Bit-Outlook. 
      
   2. Wenn Ihr Anbieter ein verwalteter Anbieter ist und Sie die Anbieterkomponente kompiliert haben, die die Zielplattform als Any **CPU** anbeigt, fahren Sie mit Schritt 6 fort, um das aktuelle Outlook-Benutzeroberflächen-Locale zu finden, um die Installation der neuesten Version des Betriebssystems vorzubereiten. Ihr Anbieter arbeitet sowohl für 32-Bit- als auch für 64-Bit-Versionen des Betriebssystems.
      
   3. Wenn Ihr Anbieter eine systemeigene COM-Komponente ist, untersuchen Sie die Bitität der installierten Version von Outlook:
      
      - Wenn die installierte Version von Outlook 32-Bit ist, muss ihr Installationsvorgang einen 32-Bit-Anbieter (in Schritt 8) installieren, nachdem sichergestellt wurde, dass ein entsprechendes BETRIEBSSYSTEM installiert ist.
      
      - Andernfalls ist die installierte Version von Outlook 64-Bit, und Das Installationsverfahren muss einen 64-Bit-Anbieter (in Schritt 8) installieren, nachdem sichergestellt wurde, dass ein entsprechendes Betriebssystem installiert ist. 
      
   4. Fahren Sie mit Schritt 6 fort, um das aktuelle Outlook zu finden, um die Installation einer geeigneten Version des Betriebssystems vorzubereiten.
    
5. **Fahren Sie mit diesem Schritt fort, wenn Outlook 2003 oder Outlook 2007** installiert ist und das Betriebssystem auf dem Clientcomputer installiert ist: Überprüfen Sie das Outlook, indem Sie den Schlüssel am folgenden Speicherort in der Windows `OSCLcid` untersuchen: 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   Der Schlüssel ist ein DWORD-Wert, der das `OSCLcid` IETF-Locale-Tag (Internet Engineering Task Force) angibt (definiert durch [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) und [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)), das das aktuelle Outlook-Benutzeroberflächen-Locale darstellt. Fahren Sie mit Schritt 7 fort, um die neueste OSC auf dem Clientcomputer zu installieren.
    
6. **Fahren Sie mit diesem Schritt fort, wenn Outlook 2003 oder Outlook 2007 installiert ist oder Outlook 2010 oder Outlook 2013 vorhanden ist, aber nicht unbedingt das neueste Betriebssystem auf dem Clientcomputer installiert ist:**
    
   Verwenden Sie **das LanguageSettings-Objekt,** um die LCID des Outlook zu bestimmen. Im folgenden Visual Basic Scripting Edition (VBScript)-Codeausschnitt wird veranschaulicht, wie Sie die LCID des Outlook-Benutzeroberflächen-Locale abrufen. 
    
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

7. **Fahren Sie mit diesem Schritt fort, wenn das Installationsprogramm über die LCID der installierten Version von Outlook verfügt, aber das neueste Betriebssystem nicht unbedingt auf dem Clientcomputer installiert ist:**
    
   Verketten Sie einen g-Link mit Ihrem Installationspaket, um sicherzustellen, dass die neueste Version des Betriebssystems auf dem Clientcomputer installiert ist. Das g-link-Format lautet wie folgt:
    
   https://g.live.com/0CR_LCID_ /  _Glink_
    
   In Tabelle 1 unten finden Sie die unterstützten _LCID-Werte_ und In Tabelle 2 die unterstützten _Glink-Werte._ Beispielsweise lautet der g-Link zum Installieren der neuesten Version des 32-Bit-BETRIEBSSYSTEMS für 32-Bit Outlook Social Connector 2013 (US Englisch): 
    
   https://g.live.com/0CR1033/82
    
8. Installieren Sie den Anbieter. Das Verfahren zur Anbieterinstallation muss den programmgesteuerten Bezeichner (ProgID) am entsprechenden Windows registrieren. Weitere Informationen finden Sie unter [Registrieren eines Anbieters](registering-a-provider.md). Stellen Sie außerdem sicher, dass die Bitität des zu installierende Anbieters mit der Bitität der Version von Outlook auf dem Clientcomputer identisch ist. Installieren Sie beispielsweise einen 32-Bit-Anbieter, wenn 32-Bit-Outlook 2013 vorhanden ist, und einen 64-Bit-Anbieter, wenn 64-Bit-Outlook 2013 installiert ist. Für Outlook 2003 oder 2007 gilt nur die 32-Bit-Version Ihres Anbieters. 
    
**Tabelle 1: Unterstütztes Locale und entsprechende LCID-Werte im Hexadezimal für das OSC**
  
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
   
**Tabelle 2: Unterstützte Glink-Werte für das OSC**
  
|**Glink-Wert**|**Funktion**|
|:-----|:-----|
|80  <br/> |Installiert die neueste Version von OSC für Outlook 2003 oder Outlook 2007.  <br/> |
|82  <br/> |Installiert den neuesten Patch von 32-Bit-OSC für Outlook 2007, Outlook 2010 oder Outlook Social Connector 2013.  <br/> |
|83  <br/> |Installiert den neuesten Patch von 64-Bit-OSC für Outlook 2010 oder Outlook Social Connector 2013.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Registrieren eines Anbieters](registering-a-provider.md) 
- [Schnelle Schritte zum Entwickeln eines Anbieters](quick-steps-for-learning-to-develop-a-provider.md)
- [Bereitstellen eines Providers](deploying-a-provider.md)

