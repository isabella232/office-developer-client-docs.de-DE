---
title: Checkliste für Installation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: In diesem Thema werden die Voraussetzungen für die erfolgreiche Installation des OSC-Anbieters (Outlook Social Connector) beschrieben, und die Installation überprüft, ob das Installationsprogramm des Anbieters ordnungsgemäß ausgeführt werden sollte.
ms.openlocfilehash: 8fec8523e57ad2678d02a0c5cbc1ad57340e5267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286340"
---
# <a name="installation-checklist"></a>Checkliste für Installation

In diesem Thema werden die Voraussetzungen für die erfolgreiche Installation des OSC-Anbieters (Outlook Social Connector) beschrieben, und die Installation überprüft, ob das Installationsprogramm des Anbieters ordnungsgemäß ausgeführt werden sollte.
  
## <a name="installation-overview"></a>Übersicht über die Installation

Benutzer sollten OSC-Anbieter nur dann installieren, wenn eine unterstützende Version von Outlook vorhanden ist und der OSC auf dem Clientcomputer installiert und aktiviert ist. Unterstützende Versionen von Outlook sind Office Outlook 2003, Office Outlook 2007, Outlook 2010 und Outlook 2013 (auf dem Clientcomputer oder, im Fall von Outlook 2010 und Outlook 2013, von Klick-und-Los auf dem Clientcomputer bereitgestellt). Zur Sicherstellungeiner erfolgreichen Installation sollte Ihr Anbieter Installationsprogramm folgende Schritte ausführen:
  
- Überprüfen Sie, ob eine unterstützte Version von Outlook vorhanden ist.
    
- Überprüfen Sie, ob OSC installiert ist.
    
> [!NOTE]
> Klick-und-los ist eine virtuelle Umgebung, in der Outlook 2010 (32-Bit) oder Outlook 2013 (32-Bit) ausgeführt werden kann. Überprüfen Sie für Outlook 2013, ob der VirtualOutlook-Schlüssel in HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook der Windows-Registrierung vorhanden ist. Weitere Informationen zum Bereitstellen von Outlook als Klick-und-Los-Produkt auf einem Clientcomputer finden Sie unter [überprüfen, ob Outlook auf einem Computer als Klick-und-Los-Produkt verfügbar ist](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx). 
  
Der Benutzer muss jedoch sicherstellen, dass OSC vor der Installation des Anbieters aktiviert ist.
  
Dritte, einschließlich OSC-Anbieter, können den OSC nicht weiterverteilen. Wenn der OSC jedoch nicht installiert ist, kann das Anbieter-Installationsprogramm mithilfe der entsprechenden g-Links den OSC auf dem Clientcomputer installieren. Ein g-Link ist eine speziell erstellte URL, https://g.live.com auf der ein Benutzer an eine entsprechende Webseite weitergeleitet wird, um den osc herunterzuladen. OSC g-Link ist als https://g.live.com/0CR _LCID_/ -_glink_formatiert, wobei _LCID_ und _glink_ das Gebietsschema, die Version und die Bitanzahl von Outlook auf dem Clientcomputer angeben. Jeder g-Link verweist auf eine ausführbare Datei und ist spezifisch für die angegebenen _LCID_ -und _glink_ -Werte. 
  
Beispielsweise lautet der g-Link zum Installieren der neuesten Version von OSC für Outlook 2003 oder Outlook 2007 für die LCID 1033 (US-Englisch) wie folgt:
  
https://g.live.com/0CR1033/80
  
Ausführliche Informationen zu _glink_ -Werten für verschiedene Versionen und Bitanzahl von Outlook sowie zu _LCID_ -Werten für unterstützte gebietsschemas finden Sie unter #7 im Abschnitt [Installationsprüfliste](#olosc_InstallationOverview_InstallationChecklist) unten. 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>Checkliste für Installation

Das Anbieter Setuppaket sollte eine Reihe von Installations Überprüfungen durchführen, wie in Abbildung 1 dargestellt, um sicherzustellen, dass der Anbieter erfolgreich installiert wird.
  
**Abbildung 1. Anbieter Installationslogik**

![Checkliste für Installation](media/odc_ol14_ta_OSC_Fig07.gif)
  
Im folgenden Verfahren werden die in Abbildung 1 beschriebenen Installations Überprüfungen beschrieben.
  
1. Ermitteln Sie als Voraussetzung, ob Outlook installiert oder vorhanden ist, und falls installiert oder vorhanden, ob die Version von Outlook den OSC unterstützt. Weitere Informationen zum Erkennen der installierten Version von Outlook finden Sie unter [Überprüfen der Outlook-Version](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx).
    
   - Wenn die installierte Version von Outlook älter als Outlook 2003 ist, kann die Anbieter Installation nicht abgeschlossen werden. Informieren Sie den Benutzer, bevor Sie mit der Installation des OSC-Anbieters fortfahren, eine unterstützte Version von Outlook und OSC zu erhalten.
    
   - Wenn Outlook nicht installiert ist, fahren Sie mit Schritt 2 fort.
    
   - Wenn Outlook 2003 oder Outlook 2007 installiert ist, fahren Sie mit Schritt 3 fort. 
    
   - Wenn Sie Outlook 2010 oder Outlook 2013 installiert haben, fahren Sie mit Schritt 4 fort.
    
2. **Führen Sie diesen Schritt aus, wenn Outlook auf dem Clientcomputer nicht installiert ist:**
    
   1. Überprüfen Sie, ob OSC als Standardkomponente einer Klick-und-Los-Installation von Outlook 2010 oder Outlook 2013 installiert ist. Untersuchen `VirtualOutlook` Sie den Schlüssel an folgendem Speicherort in der Windows-Registrierung: 
      
      - Für Outlook 2010`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - Für Outlook Connector für soziale Netzwerke 2013`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      Der `VirtualOutlook` Schlüssel ist ein REG_SZ-Wert, der das Gebietsschematag enthält, beispielsweise "en-US" des installierten Produkts. 
      
   2. Wenn der `VirtualOutlook` Schlüssel nicht vorhanden ist, ist Outlook auf dem Clientcomputer nicht vorhanden, und die Anbieter Installation kann nicht abgeschlossen werden. Informieren Sie den Benutzer, bevor Sie mit der Installation des OSC-Anbieters fortfahren, eine unterstützte Version von Outlook und OSC zu erhalten. 
      
   3. Wenn der `VirtualOutlook` Schlüssel vorhanden ist, wurde Outlook per Klick-und-Los auf dem Clientcomputer zugestellt. Gehen Sie wie folgt vor, um die installierte Version der OSC-Typbibliothek `OSCVersion` zu überprüfen, indem Sie den Schlüssel an folgendem Speicherort in der Windows-Registrierung untersuchen: 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      Der Wert von `OSCVersion` ist eine Zeichenfolge, die die Versionsnummer der Typbibliothek Socialprovider. dll angibt (beispielsweise "1,0", "1,1" oder "15"). 
      
   4. Wenn `OSCVersion` "1,0", "1,1" oder "15" ist, wird eine entsprechende Version von OSC installiert. Fahren Sie mit Schritt 6 fort, um das aktuelle Gebietsschema der Outlook-Benutzeroberfläche für die Installation der neuesten Version des OSC vorzubereiten. 
      
   5. `OSCVersion` Andernfalls enthält keinen erwarteten Wert. Fahren Sie mit Schritt 6 fort, um das aktuelle Gebietsschema der Outlook-Benutzeroberfläche für die Installation einer geeigneten Version des OSC vorzubereiten. 
    
3. **Führen Sie diesen Schritt aus, wenn Outlook 2003 oder Outlook 2007 auf dem Clientcomputer installiert ist:**
    
   1. Überprüfen Sie, ob der OSC installiert ist, indem Sie eine benutzerdefinierte Installer-Aktion schreiben, um das vorhanden sein der folgenden qualifizierten Komponenten-ID zu testen:
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      Die qualifizierte Komponenten-ID ist eine GUID, die eine Methode der Indirection mit einer Ebene bereitstellt, ähnlich wie ein Zeiger. Weitere Informationen zu Windows Installer finden Sie unter [Roadmap to Windows Installer Documentation](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation).
      
   2. Wenn die angegebene qualifizierte Komponente vorhanden ist, wird eine Version des OSC installiert. Fahren Sie mit Schritt 5 fort, um das aktuelle Gebietsschema der Outlook-Benutzeroberfläche für die Installation der neuesten Version des OSC vorzubereiten.
      
   3. Andernfalls ist der OSC nicht installiert. Fahren Sie mit Schritt 6 fort, um das aktuelle Gebietsschema der Outlook-Benutzeroberfläche für die Installation einer geeigneten Version des OSC vorzubereiten.
      
4. **Führen Sie diesen Schritt aus, wenn Outlook 2010 oder Outlook 2013 auf dem Clientcomputer installiert ist:**
    
   1. Bestimmen Sie die Bitanzahl der installierten Version von Outlook, indem Sie den `Bitness` Schlüssel an folgendem Speicherort in der Windows-Registrierung untersuchen: 
      
      - Sehen Sie sich für Outlook 2010`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - Sehen Sie sich für Outlook 2013`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      Der `Bitness` Schlüssel ist "x86" für 32-Bit-Outlook oder "x64" für 64-Bit-Outlook. 
      
   2. Wenn Ihr Anbieter ein verwalteter Anbieter ist und Sie die Anbieterkomponente kompiliert haben, die die Zielplattform als **beliebige CPU**angibt, fahren Sie mit Schritt 6 fort, um das aktuelle gebietsSchema der Outlook-Benutzeroberfläche für die Installation der neuesten Version des osc vorzubereiten. Ihr Anbieter kann sowohl 32-Bit-als auch 64-Bit-Versionen des OSC verwenden.
      
   3. Wenn es sich bei Ihrem Anbieter um eine systemeigene COM-Komponente handelt, überprüfen Sie die Bitanzahl der installierten Outlook-Version:
      
      - Wenn die installierte Version von Outlook 32-Bit ist, muss Ihr Installationsvorgang einen 32-Bit-Anbieter (in Schritt 8) installieren, nachdem Sie sichergestellt haben, dass ein entsprechender OSC installiert ist.
      
      - Andernfalls ist die installierte Version von Outlook 64-Bit, und Ihr Installationsvorgang muss einen 64-Bit-Anbieter (in Schritt 8) installieren, nachdem Sie sichergestellt haben, dass ein entsprechender OSC installiert ist. 
      
   4. Fahren Sie mit Schritt 6 fort, um das aktuelle Gebietsschema der Outlook-Benutzeroberfläche für die Installation einer geeigneten Version des OSC vorzubereiten.
    
5. Führen Sie **diesen Schritt aus, wenn outlook 2003 oder outlook 2007 installiert ist und der osc auf dem Clientcomputer installiert ist:** Überprüfen Sie das aktuelle Gebietsschema der Outlook-Benutzer `OSCLcid` Oberfläche, indem Sie den Schlüssel an folgendem Speicherort in der Windows-Registrierung untersuchen: 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   Der `OSCLcid` Schlüssel ist ein DWORD-Wert, der das Gebietsschema-Tag (Internet Engineering Task Force, IETF) (definiert durch [[rfc4646]](https://www.ietf.org/rfc/rfc4646.txt) und [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)) angibt, das das aktuelle Gebietsschema der Outlook-Benutzeroberfläche darstellt. Fahren Sie mit Schritt 7 fort, um den neuesten OSC auf dem Clientcomputer zu installieren.
    
6. **Fahren Sie mit diesem Schritt fort, wenn Outlook 2003 oder Outlook 2007 installiert ist oder Outlook 2010 oder Outlook 2013 vorhanden ist, aber der neueste OSC nicht unbedingt auf dem Clientcomputer installiert ist:**
    
   Verwenden Sie das **LanguageSettings** -Objekt, um die LCID des Gebietsschemas der Outlook-Benutzeroberfläche zu bestimmen. Der folgende Visual Basic Scripting Edition (VBScript)-Codeausschnitt veranschaulicht, wie die LCID des Outlook-Benutzeroberflächen Gebietsschemas abgerufen wird. 
    
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

7. **Fahren Sie mit diesem Schritt fort, wenn das Installationsprogramm die LCID der installierten Version von Outlook hat, aber der neueste OSC nicht unbedingt auf dem Clientcomputer installiert ist:**
    
   VerKetten Sie einen g-Link in Ihr Installationspaket, um sicherzustellen, dass die neueste Version des OSC auf dem Clientcomputer installiert ist. Das g-Link-Format lautet wie folgt:
    
   https://g.live.com/0CR_LCID_ /  _Glink_
    
   In Tabelle 1 finden Sie die unterstützten _LCID_ -Werte und Tabelle 2 für die unterStützten _glink_ -Werte. Beispielsweise lautet der g-Link, um die neueste Version des 32-Bit-OSC für 32-Bit Outlook Social Connector 2013 (US-Englisch) zu installieren: 
    
   https://g.live.com/0CR1033/82
    
8. Installieren Sie den Anbieter. Bei der Anbieter Installation muss der programmgesteuerte Bezeichner (ProgID) am entsprechenden Speicherort der Windows-Registrierung registriert werden. Weitere Informationen finden Sie unter [Registrieren eines Anbieters](registering-a-provider.md). Stellen Sie außerdem sicher, dass die Bitanzahl des zu installierenden Anbieters mit dem Bitanzahl der auf dem Clientcomputer vorhandenen Version von Outlook übereinstimmt. Installieren Sie beispielsweise einen 32-Bit-Anbieter, wenn 32-Bit Outlook 2013 vorhanden ist, und einen 64-Bit-Anbieter, falls 64-Bit Outlook 2013 installiert ist. Für Outlook 2003 oder 2007 gilt nur die 32-Bit-Version Ihres Anbieters. 
    
**Tabelle 1: unterstütztes Gebietsschema und entsprechende LCID-Werte im Hexadezimalformat für OSC**
  
|**Gebietsschema**|**LCID**|
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
|SR-Cyrl-CS  <br/> |3098  <br/> |
|SR-LATN-CS  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |
   
**Tabelle 2: Unterstützte glink-Werte für OSC**
  
|**Glink-Wert**|**Funktion**|
|:-----|:-----|
|80  <br/> |Installiert die neueste Version von OSC für Outlook 2003 oder Outlook 2007.  <br/> |
|82  <br/> |Installiert den neuesten Patch von 32-Bit OSC für Outlook 2007, Outlook 2010 oder Outlook Social Connector 2013.  <br/> |
|83  <br/> |Installiert den neuesten Patch von 64-Bit OSC für Outlook 2010 oder Outlook Social Connector 2013.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Registrieren eines Anbieters](registering-a-provider.md) 
- [Schnelle Schritte für die Entwicklung eines Anbieters](quick-steps-for-learning-to-develop-a-provider.md)
- [Bereitstellen eines Providers](deploying-a-provider.md)

