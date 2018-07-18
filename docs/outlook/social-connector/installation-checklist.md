---
title: Checkliste für Installation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: In diesem Thema werden die erforderlichen Komponenten für die Installation von einem Anbieter Outlook Social Connector (OSC) und die Installation überprüft, dass der Anbieter Installer ausführen sollten, um ordnungsgemäß funktionieren.
ms.openlocfilehash: cb8ed24db28c3b0e945c4db4b2daa4a2470d7dd5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795972"
---
# <a name="installation-checklist"></a>Checkliste für Installation

In diesem Thema werden die erforderlichen Komponenten für die Installation von einem Anbieter Outlook Social Connector (OSC) und die Installation überprüft, dass der Anbieter Installer ausführen sollten, um ordnungsgemäß funktionieren.
  
## <a name="installation-overview"></a>Übersicht über die Installation

Benutzer sollten OSC-Anbieter installieren, nur, wenn eine unterstützende Version von Outlook vorhanden ist und die OSC installiert und auf dem Clientcomputer aktiviert ist. Unterstützende Versionen von Outlook werden Office Outlook 2003, Office Outlook 2007, Outlook 2010 und Outlook 2013 (auf dem Clientcomputer oder, im Fall von Outlook 2010 und Outlook 2013, übermittelt per Klick-und-Los auf dem Clientcomputer installiert). Um eine erfolgreiche Installation zu gewährleisten, sollte das Installationsprogramm der Anbieter die Folgendes bewirken:
  
- Überprüfen Sie, ob eine unterstützte Version von Outlook vorhanden ist.
    
- Überprüfen Sie, ob die OSC installiert ist.
    
> [!NOTE]
> Klick-und-los ist eine virtuelle Umgebung in der Outlook 2010 (32-Bit) oder Outlook 2013 (32-Bit) ausgeführt werden kann. Überprüfen Sie für Outlook 2013, ob der Schlüssel virtualoutlook in der Windows-Registrierung HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook vorhanden ist. Weitere Informationen zur Bereitstellung von Outlook als Produkt Klick-und-Los auf einem Clientcomputer finden Sie unter [Vorgehensweise überprüfen, ob Outlook auf einem Computer als Klick-und-Los-Produkt verfügbar ist](http://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx). 
  
Der Benutzer hat jedoch, um sicherzustellen, dass die OSC vor der Installation des Anbieters aktiviert ist.
  
Dritte, einschließlich der OSC-Anbieter kann nicht die OSC verteilen. Wenn die OSC nicht installiert ist, können das Installationsprogramm Anbieter geeigneten g-Links jedoch die OSC auf dem Clientcomputer zu installieren. Eine g-Verknüpfung ist eine speziell erstellte URL auf http://g.live.com , die einen Benutzer zu einer entsprechenden Webseite zum Herunterladen der OSC weiterleitet. Eine OSC g-Verknüpfung ist als formatiert http://g.live.com/0CR _LCID_/ _Glink_, wobei _LCID_ und _Glink_ Gebietsschema, Version und Bitness von Outlook auf dem Clientcomputer angeben. Jede g-Link verweist auf eine ausführbare Datei und sind spezifisch für den angegebenen Werten _LCID_ und _Glink_ . 
  
Beispielsweise lautet der g-Link zur Installation der neuesten Version von der OSC für Outlook 2003 oder Outlook 2007 für die LCID 1033 (Englisch (USA)) wie folgt:
  
http://g.live.com/0CR1033/80
  
Ausführliche Informationen zu _Glink_ Werte für verschiedene Versionen und Bitness von Outlook und _LCID_ -Werte für die unterstützten Gebietsschemas finden Sie unter #7 im Abschnitt [Installationsprüfliste](#olosc_InstallationOverview_InstallationChecklist) unten. 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>Checkliste für Installation

Das Setup-Paket sollte eine Reihe von Installation Überprüfungen, ausführen, wie in Abbildung 1 dargestellt, um sicherzustellen, dass der Anbieter erfolgreich installiert.
  
**Abbildung 1. Provider-Installationslogik**

![Checkliste für Installation](media/odc_ol14_ta_OSC_Fig07.gif)
  
Das folgende Verfahren beschreibt die Installation überprüft, die in Abbildung 1 beschrieben.
  
1. Als Voraussetzung erkennen Sie, ob Outlook installiert ist oder präsentieren Sie und installierten oder vorhanden, bestimmen Sie, ob die Version von Outlook die OSC unterstützt. Weitere Informationen zum Erkennen von die installierte Version von Outlook finden Sie unter [Überprüfen der Version von Outlook](http://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx).
    
   - Wenn die installierte Version von Outlook vor Outlook 2003 liegt, kann nicht die Anbieter Installation abgeschlossen. Informieren des Benutzers zum Abrufen einer unterstützten Version von Outlook und das osc bilden, bevor Sie fortfahren, den OSC-Anbieter installieren.
    
   - Wenn Outlook nicht installiert ist, fahren Sie mit Schritt 2 fort.
    
   - Wenn Outlook 2003 oder Outlook 2007 installiert ist, fahren Sie mit Schritt 3 fort. 
    
   - Wenn Outlook 2010 oder Outlook 2013 installiert ist, fahren Sie mit Schritt 4 fort.
    
2. **Fahren Sie mit diesen Schritt, wenn Outlook auf dem Clientcomputer nicht installiert ist:**
    
   1. Überprüfen Sie, ob die OSC als Standardkomponente einer Klick-und-Los-Installation von Outlook 2010 oder Outlook 2013 installiert ist. Überprüfen Sie die `VirtualOutlook` Schlüssel in der Windows-Registrierung am folgenden Speicherort: 
      
      - Für Outlook 2010`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - Für Outlook Connector für soziale Netzwerke 2013,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      Die `VirtualOutlook` Schlüssel ist ein REG_SZ-Wert mit dem Gebietsschematag, z. B. "En-us", über das installierte Produkt. 
      
   2. Wenn die `VirtualOutlook` Schlüssel ist nicht vorhanden, Outlook nicht auf dem Clientcomputer vorhanden ist und der Anbieter Installation kann nicht abgeschlossen werden. Informieren des Benutzers zum Abrufen einer unterstützten Version von Outlook und das osc bilden, bevor Sie fortfahren, den OSC-Anbieter installieren. 
      
   3. Wenn die `VirtualOutlook` Schlüssel vorhanden ist, Outlook per Klick-und-Los auf dem Clientcomputer bereitgestellt wurde. Fahren Sie mit Überprüfen Sie die installierte Version der Typbibliothek OSC durch Untersuchen der `OSCVersion` Schlüssel an folgendem Speicherort in der Windows-Registrierung: 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      Der Wert der `OSCVersion` ist eine Zeichenfolge, die Versionsnummer der Typbibliothek von Socialprovider.dll (z. B. "1.0", "1.1" oder "15") angibt. 
      
   4. Wenn `OSCVersion` "1.0", "1.1" oder "15" ist, wird eine entsprechende OSC-Version installiert ist. Fahren Sie mit Schritt 6, um das aktuelle Outlook Gebietsschema der Benutzeroberfläche zur Vorbereitung der Installation der aktuellen Version von der OSC suchen. 
      
   5. Andernfalls `OSCVersion` enthält einen erwartete Wert nicht. Fahren Sie mit Schritt 6, um das aktuelle Outlook Gebietsschema der Benutzeroberfläche zur Vorbereitung der Installation einer entsprechenden Version der die OSC suchen. 
    
3. **Fahren Sie mit diesen Schritt, wenn Outlook 2003 oder Outlook 2007 auf dem Clientcomputer installiert ist:**
    
   1. Überprüfen Sie, ob die OSC installiert ist, indem Sie einen Installer schreiben benutzerdefinierte Aktion, um das Vorhandensein der folgenden gekennzeichneten Komponenten-ID:
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      Die gekennzeichneten Komponenten-ID ist eine GUID, die eine Methode der einstufigen Dereferenzierung, ähnlich einem Zeiger bereitgestellt. Weitere Informationen zu Windows Installer finden Sie unter [Übersicht über die Windows Installer-Dokumentation](http://msdn.microsoft.com/library/_msi_roadmap_to_windows_installer_documentation.aspx).
      
   2. Wenn die angegebene qualifizierte Komponente vorhanden ist, wird eine Version der die OSC installiert. Wechseln Sie zu Schritt 5, um das aktuelle Outlook Gebietsschema der Benutzeroberfläche zur Vorbereitung der Installation der aktuellen Version von der OSC suchen.
      
   3. Andernfalls wird die OSC nicht installiert. Fahren Sie mit Schritt 6, um das aktuelle Outlook Gebietsschema der Benutzeroberfläche zur Vorbereitung der Installation einer entsprechenden Version der die OSC suchen.
      
4. **Fahren Sie mit diesen Schritt, wenn Outlook 2010 oder Outlook 2013 auf dem Clientcomputer installiert ist:**
    
   1. Bestimmen die Bitness der installierten Version von Outlook durch Untersuchen der `Bitness` Schlüssel in der Windows-Registrierung am folgenden Speicherort: 
      
      - Sehen Sie sich für Outlook 2010`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - Sehen Sie sich für Outlook 2013`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      Die `Bitness` Schlüssel "X86" für 32-Bit-Outlook oder "X64" für 64-Bit-Outlook ist. 
      
   2. Wenn der Anbieter einen verwalteten Anbieter ist und Sie kompiliert der Anbieterkomponente angeben der Zielplattform **Any**CPU, fahren Sie mit Schritt 6 aus, um das aktuelle Outlook Gebietsschema der Benutzeroberfläche zur Vorbereitung der Installation der aktuellen Version von der OSC suchen. Vom Dienstanbieter funktioniert auf 32-Bit- und 64-Bit-Versionen von der OSC.
      
   3. Wenn der Anbieter eine systemeigene COM-Komponente ist, untersuchen Sie die Bitness der installierten Version von Outlook:
      
      - Ist die installierte Version von Outlook auf 32-Bit, müssen Ihre Installationsvorgang installieren einen 32-Bit-Anbieter (in Schritt 8), stellen Sie sicher, dass eine entsprechende OSC installiert ist.
      
      - Sie andernfalls die installierte Version von Outlook ist 64-Bit- und Ihre Installationsverfahren muss einen 64-Bit-Anbieter (in Schritt 8) zu installieren, stellen Sie sicher, dass eine entsprechende OSC installiert ist. 
      
   4. Fahren Sie mit Schritt 6 aus, um das aktuelle Outlook Gebietsschema der Benutzeroberfläche zur Vorbereitung der Installation einer entsprechenden Version der die OSC suchen.
    
5. **Mit diesem Schritt fortgesetzt werden, wenn Outlook 2003 oder Outlook 2007 installiert ist, und die OSC auf dem Clientcomputer installiert ist:** Überprüfen Sie das aktuelle Gebietsschema der Benutzeroberfläche Outlook durch Untersuchen der `OSCLcid` Schlüssel in der Windows-Registrierung am folgenden Speicherort: 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   Die `OSCLcid` Schlüssel ist ein DWORD-Wert, die der Internet Engineering Task Force (IETF) Gebietsschematag (definiert durch [[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) und [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt)), gibt an, die das aktuelle Gebietsschema der Benutzeroberfläche Outlook darstellt. Fahren Sie mit Schritt 7, um die neuesten OSC auf dem Clientcomputer zu installieren.
    
6. **Fahren Sie mit diesen Schritt, wenn Outlook 2003 oder Outlook 2007 installiert ist, oder Outlook 2010 oder Outlook 2013 vorhanden ist, aber die neuesten OSC nicht unbedingt auf dem Clientcomputer installiert ist:**
    
   Verwenden Sie das **LanguageSettings** -Objekt, um die LCID der Outlook-Schnittstelle vom Gebietsschema des Benutzers zu bestimmen. Im folgende Visual Basic Scripting Edition (VBScript) Codeausschnitt veranschaulicht, wie die LCID der das Gebietsschema der Benutzeroberfläche Outlook zu erhalten. 
    
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

7. **Fahren Sie mit diesen Schritt das Installationsprogramm hat die LCID der installierten Version von Outlook, jedoch nicht die neuesten OSC nicht unbedingt auf dem Clientcomputer installiert ist:**
    
   Verketten Sie eine g-Verknüpfung mit dem Installationspaket, um sicherzustellen, dass die neueste Version von der OSC auf dem Clientcomputer installiert ist. Das g LinkFormat-Objekt lautet wie folgt:
    
   http://g.live.com/0CR_LCID_ /  _Glink_
    
   Finden Sie in Tabelle 1 weiter unten sind die unterstützten _LCID_ -Werte und Tabelle 2 für die unterstützten _Glink_ Werte. Beispielsweise lautet der g-Link So installieren Sie die neueste Version von der 32-Bit-OSC für 32-Bit-Outlook Social Connector 2013 (Englisch (USA)) wie folgt: 
    
   http://g.live.com/0CR1033/82
    
8. Installieren Sie den Anbieter. Das Installationsverfahren Anbieter muss die programmkennung (ProgID) an der entsprechenden Stelle der Windows-Registrierung registrieren. Weitere Informationen finden Sie unter [Registrieren eines Anbieters](registering-a-provider.md). Außerdem sicher, dass die Bitness des Anbieters zu installierende identisch mit der Bitness der Version von Outlook auf dem Clientcomputer vorhanden ist sein. Installieren Sie 32-Bit-Anbieter Wenn 32-Bit-Outlook 2013 vorhanden ist und eine 64-Bit-Anbieter Wenn 64-Bit-Outlook 2013 installiert ist. Für Outlook 2003 oder 2007 gilt nur die 32-Bit-Version des Anbieters. 
    
**Tabelle 1: Unterstützte Gebietsschemas und entsprechende LCID-Werte für das osc bilden hexadezimal**
  
|**Gebietsschema**|**LCID**|
|:-----|:-----|
|ar-sa  <br/> |1025  <br/> |
|bg-bg  <br/> |1026  <br/> |
|CA-es  <br/> |1027  <br/> |
|cs-cz  <br/> |1029  <br/> |
|da-dk  <br/> |1030  <br/> |
|de-de  <br/> |1031  <br/> |
|el-gr  <br/> |1032  <br/> |
|en-us  <br/> |1033  <br/> |
|es-es  <br/> |3082  <br/> |
|et-ee  <br/> |1061  <br/> |
|EU-es  <br/> |1069  <br/> |
|fi-fi  <br/> |1035  <br/> |
|fr-fr  <br/> |1036  <br/> |
|GL-es  <br/> |1110  <br/> |
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
|SR-Cyrl-cs  <br/> |3098  <br/> |
|SR-Latn-cs  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |
   
**Tabelle 2: Unterstützte Glink Werte für das osc bilden**
  
|**GLINK Wert**|**Funktion**|
|:-----|:-----|
|80  <br/> |Die neueste Version von OSC für Outlook 2003 oder Outlook 2007 installiert.  <br/> |
|82  <br/> |Installiert den neuesten Patch von 32-Bit-OSC für Outlook 2007, Outlook 2010 oder Outlook Social Connector 2013.  <br/> |
|83  <br/> |Das neueste OSC für Outlook 2010 oder Outlook Social Connector 2013 64-Bit-Patch installiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Registrieren eines Providers](registering-a-provider.md) 
- [QuickSteps für Informationen zum Entwickeln eines Providers](quick-steps-for-learning-to-develop-a-provider.md)
- [Bereitstellen eines Providers](deploying-a-provider.md)

