---
title: Veröffentlichen von Formularen mit Code
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: caafab24-6413-4731-813d-cba3ae9ea97e
description: Alle Websitesammlungs-Administrator kann Formularen mit Code direkt in InfoPath Designer Veröffentlichungs-Assistenten in einer Formularbibliothek in SharePoint veröffentlichen. Der Code wird in einem Sandkasten-Umgebung ausgeführt, sodass den Server nicht bösartiger Code beschädigen kann. Dies wird als Veröffentlichen einer sandkastenlösung oder beim Veröffentlichen der SharePoint-Infrastruktur Sandbox bezeichnet.
ms.openlocfilehash: c25243a966bc1dc1a559ccf2ba58fabfadbd94a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790844"
---
# <a name="publishing-forms-with-code"></a>Veröffentlichen von Formularen mit Code

Alle Websitesammlungs-Administrator kann Formularen mit Code direkt in InfoPath Designer Veröffentlichungs-Assistenten in einer Formularbibliothek in SharePoint veröffentlichen. Der Code wird in einem Sandkasten-Umgebung ausgeführt, sodass den Server nicht bösartiger Code beschädigen kann. Dies wird als Veröffentlichen einer sandkastenlösung oder beim Veröffentlichen der SharePoint-Infrastruktur Sandbox bezeichnet.
  
InfoPath 2010 und SharePoint Server 2010 unterstützt auch vom Administrator bereitgestellte Lösungen. Ein Formular-Designer veröffentlicht Formularen mit Code eines lokalen Speichers die weiter unten überprüft und von einem SharePoint-Farmadministrator hochgeladen werden. Der Code erhält die volle Vertrauenswürdigkeit und Funktionalität wie etwa e/a-Datei erhöhte Berechtigungen anfordern integrieren kann.
  
## <a name="comparing-sandboxed-and-administrator-approved-solutions"></a>Vergleich zwischen Sandkastenlösungen und vom Administrator genehmigten Lösungen

In der folgenden Tabelle werden die Unterschiede zwischen dem Veröffentlichen von Sandkastenlösungen und von vom Administrator genehmigten Lösungen beschrieben.  
  
||**Sandkastenlösungen (engl.)**|**Vom Administrator genehmigte Lösungen**|
|:-----|:-----|:-----|
|**Erforderliche Berechtigungen** <br/> |Kann von jedem Websitesammlungsadministrator veröffentlicht werden.  <br/> |Kann von einem Farmadministrator bereitgestellt werden.  <br/> |
|**Veröffentlichen** <br/> |Kann direkt in InfoPath veröffentlicht werden.  <br/> |Kann mithilfe der Zentraladministration oder des Befehlszeilentools stsadm bereitgestellt werden.  <br/> |
|**Protection** <br/> |Code wird in einer Sandkastenumgebung ausgeführt. Dadurch wird der Server vor bösartigem Code geschützt.  <br/> |Code kann mit voller Vertrauenswürdigkeit ausgeführt werden und auf alle Ressourcen auf dem Server zugreifen.  <br/> |
|**Empfohlene Verwendung** <br/> |Formulare, für die nur in geringem Umfang Code benötigt wird.  <br/> |Formulare, die viele Codezeilen enthalten.  <br/> |
   
### <a name="publishing-form-templates-as-sandboxed-solutions"></a>Veröffentlichen von Formularvorlagen als Sandkastenlösungen

Veröffentlichen eines Formulars mithilfe von Code als sandkastenlösung unterscheidet sich nicht von einer anderen Form in einer Dokumentbibliothek veröffentlichen. Verwenden Sie den Veröffentlichen-Assistenten nur wie gewohnt und das Formular wird auf den Server hochgeladen werden und funktionieren in der sandkastenlösung.
  
Beachten Sie, dass bestimmte Einschränkungen Bereitstellung eines Formulars als sandkastenlösung:
  
- Muss ein InfoPath-Formular.
    
- Als Programmiersprache muss C# oder Visual Basic verwendet werden.
    
- E-Mail-datenverbindungen nicht gesendet werden.
    
- Es ist nicht möglich, Eigenschaften für Webpart-zu-Webpart-Verbindungen heraufzustufen.
    
- Es dürfen keine Steuerelemente für verwaltete Metadaten oder Datenverbindungen verwendet werden.
    
Zum Aktivieren von Websitesammlungsadministratoren Lösungen mit eingeschränkter Sicherheitsstufe auf Microsoft SharePoint Server 2010 oder einem Server mit Microsoft SharePoint Foundation 2010 verwenden, muss der Farmadministrator den Windows SharePoint-benutzercodedienst starten.
  
### <a name="to-start-the-windows-sharepoint-user-code-service"></a>So starten Sie den Windows SharePoint-Benutzercodedienst

1. Öffnen Sie die Zentraladministration.
    
2. Klicken Sie unter **Systemdienste**auf **Dienste auf dem Server verwalten**.
    
3. Starten Sie den **Microsoft SharePoint Foundation-Benutzercodedienst**.
    
### <a name="to-publish-a-sandboxed-solution"></a>So veröffentlichen Sie eine Sandkastenlösung

1. Öffnen Sie die Formularvorlage in InfoPath Designer.
    
2. Klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf **SharePoint Server** auf der Registerkarte **Veröffentlichen** in der Backstage-Ansicht. 
    
3. Geben Sie die URL der SharePoint-Website veröffentlichen, und klicken Sie dann auf **Weiter**. 
    
    > [!IMPORTANT]
    > Sie müssen ein Websitesammlungsadministrator auf dieser Website zum Veröffentlichen dieser Formularvorlage als sandkastenlösung sein. 
  
4. Wählen Sie **Formularbibliothek**aus, und klicken Sie dann auf **Weiter**.
    
5. Wählen Sie **eine neue Formularbibliothek erstellen**aus, und klicken Sie dann auf **Weiter**.
    
6. Geben Sie den Namen und eine Beschreibung für die Formularbibliothek ein, und klicken Sie dann auf **Weiter**.
    
7. Klicken Sie auf **Veröffentlichen**.
    
Beispiel: Lösungen, die Szenarien veranschaulicht, die für Formularvorlagen als sandkastenlösungen veröffentlicht geeignet sind [Beispiele für Sandkastenlösungen](sample-sandboxed-solutions.md)angezeigt.
  
### <a name="publishing-form-templates-as-administrator-deployed-solutions"></a>Veröffentlichen von Formularvorlagen als vom Administrator bereitgestellte Lösungen

Das Veröffentlichen eines Formulars als vom Administrator genehmigte Vorlage wird empfohlen, wenn das Formular zahlreiche Datenverbindungen enthält, wenn Sicherheit durch volle Vertrauenswürdigkeit erforderlich ist oder wenn Sie eine farmweite Vorlage benötigen.
  
Ein Farmadministrator muss verschiedene Schritte ausführen, bevor eine vom Administrator bereitgestellte Lösung in SharePoint verfügbar ist. Sie als Entwickler müssen die Lösung vorbereiten, bevor der Administrator hinzugezogen wird.
  
Wenn das Formular als voll vertrauenswürdig bereitgestellt werden soll, müssen Sie zuerst die Sicherheitsstufe wie im folgenden Verfahren beschrieben festlegen.
  
### <a name="to-set-the-security-level-of-a-form-template-to-full-trust"></a>So legen Sie die Sicherheitsstufe einer Formularvorlage auf "Voll vertrauenswürdig" fest

1. Öffnen Sie die Formularvorlage in InfoPath Designer.
    
2. Klicken Sie auf der Registerkarte **Datei** , klicken Sie auf der Registerkarte **Info** auf **Formularoptionen**.
    
3. Klicken Sie auf die Kategorie **Sicherheit und Vertrauensstellung** , und klicken Sie dann das Kontrollkästchen Sie **Sicherheitsstufe automatisch ermitteln** . 
    
4. Wählen Sie **voll vertrauenswürdig**aus.
    
Veröffentlichen Sie dann das Formular mithilfe des folgenden Verfahrens. Beachten Sie dabei, dass dabei Unterschiede zu einem Standardveröffentlichungsverfahren bestehen.
  
### <a name="to-publish-an-administrator-deployed-solution"></a>So veröffentlichen Sie eine vom Administrator bereitgestellte Lösung

1. Klicken Sie in der ersten Seite des **Veröffentlichungs-Assistenten**Geben Sie den Speicherort der SharePoint Server 2010 oder SharePoint Foundation 2010-Website, und klicken Sie dann auf **Weiter**.
    
2. InfoPath wählt automatisch auf der zweiten Seite des Assistenten das Kontrollkästchen **vom Administrator genehmigten Formularvorlage** . Klicken Sie auf **Weiter**.
    
3. Die dritte Seite gilt nur für vom Administrator bereitgestellte Szenarien. Veröffentlichen Sie das Formular auf einem lokalen Speicher, anstatt einen SharePoint-Server. Der SharePoint-Administrator, während der Bereitstellung vom Administrator die Datei aus diesem Speicherort hochgeladen werden.
    
4. Führen Sie die restlichen Seiten des **Veröffentlichungs-Assistenten**.
    

