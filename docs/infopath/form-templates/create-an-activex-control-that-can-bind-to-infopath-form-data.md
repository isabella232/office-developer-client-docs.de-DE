---
title: Erstellen eines ActiveX-Steuerelements, das an InfoPath-Formulardaten gebunden werden kann
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: Sie können ActiveX-Steuerelementen in InfoPath-Formulare hosten, die in der InfoPath-Editor geöffnet werden soll. Diese Steuerelemente können (mit einigen Einschränkungen) bereits vorhandene werden oder speziell für InfoPath geschrieben werden können.
ms.openlocfilehash: 90378533a7c3cde4a1927753c0325fdd8d0b3ce5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790725"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a>Erstellen eines ActiveX-Steuerelements, das an InfoPath-Formulardaten gebunden werden kann

Sie können ActiveX-Steuerelementen in InfoPath-Formulare hosten, die in der InfoPath-Editor geöffnet werden soll. Diese Steuerelemente können (mit einigen Einschränkungen) bereits vorhandene werden oder speziell für InfoPath geschrieben werden können.
  
## <a name="write-an-activex-control"></a>Schreiben eines ActiveX-Steuerelements

Wie andere Steuerelemente in InfoPath sollten ActiveX-Steuerelemente vorhandene Component Object Model (COM) Schnittstellen unterstützen:
  
- **IDispatch**
    
- **IPersistPropertyBag**
    
- **IPersistStreamInit**
    
- **IPropertyPage-Schnittstelle**
    
- **IObjectSafety**
    
- **IPropertyNotifySink**
    
- **Die IViewObject**
    
- **IOleObject**
    
- **IOleInPlaceObject**
    
Damit InfoPath Eigenschaften in das Modell DOM (Document Object) zum Zeitpunkt aktualisiert, die sie im Steuerelement ändern kann, sollte das Steuerelement die folgenden Schnittstellen implementieren:
  
- **IConnectionPointContainer**
    
- **IEnumConnectionPoints**
    
- **IConnectionPoint**
    
- **IEnumConnections**
    
Es gibt auch zwei InfoPath-spezifische COM-Schnittstellen, die eine engere Integration von Steuerelementen ermöglichen:
  
- [IInfoPathControl](http://msdn.microsoft.com/en-us/library/bb264625.aspx)
    
- [IInfoPathControlSite](http://msdn.microsoft.com/en-us/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a>Hinzufügen eines ActiveX-Steuerelements zur InfoPath-Entwicklungsumgebung

Der **Steuerelemente hinzufügen oder Entfernen benutzerdefinierter** Befehl auf dem Aufgabenbereich **Steuerelemente** können Sie mithilfe des **Assistenten zum Hinzufügen eines benutzerdefinierten Steuerelements** ein benutzerdefiniertes Steuerelement hinzugefügt. Mithilfe des Assistenten können Sie ein ActiveX-Steuerelement auswählen, die bereits registriert wurde oder zusätzliche benutzerdefinierte Steuerelemente auf Office Marketplace finden. Nachdem Sie ein Steuerelement ausgewählt haben, können Sie die folgenden Elemente angeben. 
  
- Angeben einer CAB-Datei zum Installieren des ActiveX-Steuerelements mit der Formularvorlage
    
- Angeben einer Bindungseigenschaft zum Binden an die XML-Daten
    
- Angeben einer Eigenschaft, die zum Aktivieren oder Deaktivieren des Steuerelements als Reaktion auf Regeln oder digitale Signaturen verwendet wird, was beispielsweise hilfreich sein kann, wenn die XML-Daten nicht vorhanden sind oder wenn bedingte Formatierung verwendet wird
    
- Angeben der Datentypbindung
    
> [!NOTE]
> Wenn Sie ein ActiveX-Steuerelement entwickeln und es dem Aufgabenbereich **Steuerelemente** in InfoPath hinzugefügt haben, können Sie das ActiveX-Steuerelement neu erstellen, bis InfoPath geschlossen wird. 
  
## <a name="deploy-an-activex-control"></a>Bereitstellen eines ActiveX-Steuerelements

Um ein ActiveX-Steuerelement zu verteilen, können Sie ein Installationsprogramm, das das Steuerelement auf dem Zielcomputer installiert wird und kopiert die Vorlage (ICT Datei InfoPath Control) und der CAB-Datei in den Ordner des Benutzers, Schreiben \Users\\< Username\>\AppData\Local\ Microsoft\InfoPath\Controls. Beachten Sie, dass, wenn mindestens zwei Entwickler sind zur Entwicklung von Formularen, die ActiveX-Steuerelemente verwenden zusammenarbeiten, jedes Entwicklers sollte die Steuerelemente, die das InfoPath-Design-Umgebung hinzugefügt wurden, oder nicht zum Ändern der Eigenschaften der Steuerelemente aus InfoPath.
  
## <a name="see-also"></a>Siehe auch



Übung 6: Hinzufügen von ActiveX-Steuerelementen in InfoPath 2003
  
[Erstellen von benutzerdefinierten InfoPath-Steuerelements mit c# und .NET (Blog des InfoPath-Teams)](http://blogs.msdn.com/infopath/archive/2005/04/15/creating-an-infopath-custom-control-using-c-and-net.aspx)

