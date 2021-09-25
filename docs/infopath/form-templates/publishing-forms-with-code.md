---
title: Veröffentlichen von Formularen mit Code
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: caafab24-6413-4731-813d-cba3ae9ea97e
description: Jeder Websitesammlungsadministrator kann Formulare mit Code direkt aus dem InfoPath Designer-Veröffentlichungs-Assistenten in einer Formularbibliothek auf SharePoint veröffentlichen. Der Code wird in einer Sandkastenumgebung ausgeführt, damit der Server nicht durch bösartigen Code geschädigt werden kann. Dies wird als Veröffentlichen einer Sandkastenlösung oder Veröffentlichen in der SharePoint-Sandkasteninfrastruktur bezeichnet.
ms.openlocfilehash: ddc224826650ecda8f54bc7d882b78bc90377b81
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557435"
---
# <a name="publishing-forms-with-code"></a>Veröffentlichen von Formularen mit Code

Jeder Websitesammlungsadministrator kann Formulare mit Code direkt aus dem InfoPath Designer-Veröffentlichungs-Assistenten in einer Formularbibliothek auf SharePoint veröffentlichen. Der Code wird in einer Sandkastenumgebung ausgeführt, damit der Server nicht durch bösartigen Code geschädigt werden kann. Dies wird als Veröffentlichen einer Sandkastenlösung oder Veröffentlichen in der SharePoint-Sandkasteninfrastruktur bezeichnet.
  
InfoPath 2010 und SharePoint Server 2010 unterstützen auch vom Administrator bereitgestellte Lösungen. Ein Formulardesigner veröffentlicht in einem lokalen Speicher Formulare mit Code, die später von einem SharePoint-Farmadministrator überprüft und hochgeladen werden. Der Code wird als voll vertrauenswürdig eingestuft und kann Funktionalität enthalten, für die erhöhte Berechtigungen wie beispielsweise Datei-E/A erforderlich sind.
  
## <a name="comparing-sandboxed-and-administrator-approved-solutions"></a>Vergleich zwischen Sandkastenlösungen und vom Administrator genehmigten Lösungen

In der folgenden Tabelle werden die Unterschiede zwischen dem Veröffentlichen von Sandkastenlösungen und von vom Administrator genehmigten Lösungen beschrieben.  
  
||**Sandkastenlösungen**|**Vom Administrator genehmigte Lösungen**|
|:-----|:-----|:-----|
|**Erforderliche Berechtigungen** <br/> |Kann von jedem Websitesammlungsadministrator veröffentlicht werden.  <br/> |Kann von einem Farmadministrator bereitgestellt werden.  <br/> |
|**Publishing** <br/> |Kann direkt über InfoPath veröffentlicht werden.  <br/> |Kann mithilfe der Zentraladministration oder des Befehlszeilentools stsadm bereitgestellt werden.  <br/> |
|**Schutz** <br/> |Code wird in einer Sandkastenumgebung ausgeführt. Dadurch wird der Server vor bösartigem Code geschützt.  <br/> |Code kann mit voller Vertrauenswürdigkeit ausgeführt werden und auf alle Ressourcen auf dem Server zugreifen.  <br/> |
|**Empfohlene Verwendung** <br/> |Formulare, für die nur in geringem Umfang Code benötigt wird.  <br/> |Formulare, die viele Codezeilen enthalten.  <br/> |
   
### <a name="publishing-form-templates-as-sandboxed-solutions"></a>Veröffentlichen von Formularvorlagen als Sandkastenlösungen

Das Veröffentlichen eines Formulars mit Code als Sandkastenlösung unterscheidet sich nicht von der Veröffentlichung eines anderen Formulars in einer Dokumentbibliothek. Verwenden Sie einfach wie gewohnt den Veröffentlichungs-Assistenten, und das Formular wird auf den Server hochgeladen und kann im Sandkasten verwendet werden.
  
Beachten Sie, dass es bestimmte Einschränkungen für die Bereitstellung Ihres Formulars als Sandkastenlösung gibt:
  
- Muss ein InfoPath-Formular sein.
    
- Als Programmiersprache muss C# oder Visual Basic verwendet werden.
    
- An E-Mail-Datenverbindungen kann nicht gesendet werden.
    
- Es ist nicht möglich, Eigenschaften für Webpart-zu-Webpart-Verbindungen heraufzustufen.
    
- Es dürfen keine Steuerelemente für verwaltete Metadaten oder Datenverbindungen verwendet werden.
    
Damit Websitesammlungsadministratoren Sandkastenlösungen auf Microsoft SharePoint Server 2010 oder einem Server verwenden können, der Microsoft SharePoint Foundation 2010 ausgeführt wird, muss der Farmadministrator den Windows SharePoint Benutzercodedienst starten.
  
### <a name="to-start-the-windows-sharepoint-user-code-service"></a>So starten Sie den Windows SharePoint-Benutzercodedienst

1. Öffnen Sie die Zentraladministration.
    
2. Klicken Sie unter **Systemdienste** auf **Dienste auf dem Server verwalten**.
    
3. Starten Sie den **Microsoft SharePoint Foundation-Benutzercodedienst**.
    
### <a name="to-publish-a-sandboxed-solution"></a>So veröffentlichen Sie eine Sandkastenlösung

1. Öffnen Sie die Formularvorlage in InfoPath Designer.
    
2. Klicken Sie auf die Registerkarte **"Datei"** und dann auf der Registerkarte **"Veröffentlichen"** in backstage auf **SharePoint Server.** 
    
3. Geben Sie die URL der SharePoint-Website ein, auf der das Formular veröffentlicht werden soll, und klicken Sie dann auf **Weiter**. 
    
    > [!IMPORTANT]
    > Sie müssen ein Websitesammlungsadministrator auf dieser Website sein, um diese Formularvorlage als Sandkastenlösung zu veröffentlichen. 
  
4. Wählen Sie **Formularbibliothek** aus, und klicken Sie dann auf **Weiter**.
    
5. Wählen Sie **Neue Formularbibliothek erstellen** aus, und klicken Sie dann auf **Weiter**.
    
6. Geben Sie den Namen und die Beschreibungen für die Formularbibliothek ein, und klicken Sie dann auf **Weiter**.
    
7. Klicken Sie auf **Veröffentlichen**.
    
Beispiellösungen, die Szenarien veranschaulichen, die für Formularvorlagen geeignet sind, die als Sandkastenlösungen veröffentlicht wurden, finden Sie unter ["Beispiel-Sandkastenlösungen".](sample-sandboxed-solutions.md)
  
### <a name="publishing-form-templates-as-administrator-deployed-solutions"></a>Veröffentlichen von Formularvorlagen als vom Administrator bereitgestellte Lösungen

Das Veröffentlichen eines Formulars als vom Administrator genehmigte Vorlage wird empfohlen, wenn das Formular zahlreiche Datenverbindungen enthält, wenn Sicherheit durch volle Vertrauenswürdigkeit erforderlich ist oder wenn Sie eine farmweite Vorlage benötigen.
  
Ein Farmadministrator muss verschiedene Schritte ausführen, bevor eine vom Administrator bereitgestellte Lösung in SharePoint verfügbar ist. Sie als Entwickler müssen die Lösung vorbereiten, bevor der Administrator hinzugezogen wird.
  
Wenn das Formular als voll vertrauenswürdig bereitgestellt werden soll, müssen Sie zuerst die Sicherheitsstufe wie im folgenden Verfahren beschrieben festlegen.
  
### <a name="to-set-the-security-level-of-a-form-template-to-full-trust"></a>So legen Sie die Sicherheitsstufe einer Formularvorlage auf "Voll vertrauenswürdig" fest

1. Öffnen Sie die Formularvorlage in InfoPath Designer.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie auf der Registerkarte **Info** auf **Formularoptionen**.
    
3. Klicken Sie auf die Kategorie **Sicherheit und Vertrauensstellung**, und deaktivieren Sie dann das Kontrollkästchen **Sicherheitsstufe automatisch ermitteln**. 
    
4. Wählen Sie **Voll vertrauenswürdig** aus.
    
Veröffentlichen Sie dann das Formular mithilfe des folgenden Verfahrens. Beachten Sie dabei, dass dabei Unterschiede zu einem Standardveröffentlichungsverfahren bestehen.
  
### <a name="to-publish-an-administrator-deployed-solution"></a>So veröffentlichen Sie eine vom Administrator bereitgestellte Lösung

1. Geben Sie auf der ersten Seite des **Veröffentlichungs-Assistenten** den Speicherort der Website SharePoint Server 2010 oder SharePoint Foundation 2010 an, und klicken Sie dann auf **"Weiter".**
    
2. InfoPath aktiviert automatisch das Kontrollkästchen für vom **Administrator genehmigte Formularvorlagen** auf der zweiten Seite des Assistenten. Klicken Sie auf **Weiter**.
    
3. Die dritte Seite gilt nur für Szenarien mit Bereitstellung durch den Administrator. Anstatt einen SharePoint Server auszuwählen, veröffentlichen Sie das Formular in einem lokalen Speicher. Der SharePoint-Administrator lädt die Datei während des Bereitstellungsvorgangs aus diesem Speicherort hoch.
    
4. Schließen Sie die restlichen Seiten des Veröffentlichungs-Assistenten ab.
    

