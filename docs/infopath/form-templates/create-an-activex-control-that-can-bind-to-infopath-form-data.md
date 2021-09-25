---
title: Erstellen eines ActiveX-Steuerelements, das an InfoPath-Formulardaten gebunden werden kann
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: Sie können ActiveX Steuerelemente in InfoPath-Formularen hosten, die im InfoPath-Editor geöffnet werden sollen. Diese Steuerelemente können bereits vorhanden sein (mit einigen Einschränkungen) oder speziell für InfoPath geschrieben werden.
ms.openlocfilehash: 8a5d19da95e9342182760256891e5701b2ab8a41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568159"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a>Erstellen eines ActiveX-Steuerelements, das an InfoPath-Formulardaten gebunden werden kann

Sie können ActiveX Steuerelemente in InfoPath-Formularen hosten, die im InfoPath-Editor geöffnet werden sollen. Diese Steuerelemente können bereits vorhanden sein (mit einigen Einschränkungen) oder speziell für InfoPath geschrieben werden.
  
## <a name="write-an-activex-control"></a>Schreiben eines ActiveX-Steuerelements

Wie bei anderen Steuerelementen in InfoPath sollten ActiveX Steuerelemente vorhandene COM-Schnittstellen (Component Object Model) unterstützen:
  
- **Idispatch**
    
- **IPersistPropertyBag**
    
- **IPersistStreamInit**
    
- **IPropertyPage**
    
- **IObjectSafety**
    
- **Ipropertynotifysink**
    
- **IViewObject**
    
- **IOleObject**
    
- **IOleInPlaceObject**
    
Damit InfoPath die Eigenschaften im Dom (Document Object Model) zum Zeitpunkt der Änderung im Steuerelement aktualisieren kann, sollte das Steuerelement die folgenden Schnittstellen implementieren:
  
- **Iconnectionpointcontainer**
    
- **IEnumConnectionPoints**
    
- **Iconnectionpoint**
    
- **IEnumConnections**
    
Außerdem gibt es zwei InfoPath-spezifische COM-Schnittstellen, die eine strengere Integration von Steuerelementen ermöglichen:
  
- [IInfoPathControl](https://msdn.microsoft.com/library/bb264625.aspx)
    
- [IInfoPathControlSite](https://msdn.microsoft.com/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a>Hinzufügen eines ActiveX-Steuerelements zur InfoPath-Entwicklungsumgebung

Mit dem Befehl **"Benutzerdefinierte Steuerelemente hinzufügen" oder "Benutzerdefinierte Steuerelemente entfernen"** im Aufgabenbereich **"Steuerelemente"** können Sie den Assistenten zum **Hinzufügen von benutzerdefinierten Steuerelementen** verwenden, um ein benutzerdefiniertes Steuerelement hinzuzufügen. Mithilfe des Assistenten können Sie ein ActiveX Steuerelement auswählen, das bereits registriert wurde, oder zusätzliche benutzerdefinierte Steuerelemente auf Office Marketplace finden. Nachdem Sie ein Steuerelement ausgewählt haben, können Sie die folgenden Elemente angeben. 
  
- Angeben einer CAB-Datei zum Installieren des ActiveX-Steuerelements mit der Formularvorlage
    
- Angeben einer Bindungseigenschaft zum Binden an die XML-Daten
    
- Angeben einer Eigenschaft, die zum Aktivieren oder Deaktivieren des Steuerelements als Reaktion auf Regeln oder digitale Signaturen verwendet wird, was beispielsweise hilfreich sein kann, wenn die XML-Daten nicht vorhanden sind oder wenn bedingte Formatierung verwendet wird
    
- Angeben der Datentypbindung
    
> [!NOTE]
> Wenn Sie ein ActiveX-Steuerelement entwickeln und es dem Aufgabenbereich **"Steuerelemente"** in InfoPath hinzugefügt haben, können Sie das ActiveX Steuerelement erst neu erstellen, wenn InfoPath geschlossen wird. 
  
## <a name="deploy-an-activex-control"></a>Bereitstellen eines ActiveX-Steuerelements

Um ein ActiveX Steuerelement zu verteilen, können Sie ein Installationsprogramm schreiben, das das Steuerelement auf dem Zielcomputer installiert und die InfoPath Control Template (ICT)-Datei und die CAB-Datei in den Ordner "\Benutzer \\<Benutzername \> \AppData\Local\Microsoft\InfoPath\Controls" kopiert. Wenn zwei oder mehr Entwickler an der Entwicklung von Formularen zusammenarbeiten, die ActiveX Steuerelemente verwenden, sollte jeder Entwickler über die Steuerelemente verfügen, die der InfoPath-Entwurfsumgebung hinzugefügt wurden, oder sie können die Eigenschaften der Steuerelemente aus InfoPath nicht ändern.
  
## <a name="see-also"></a>Siehe auch

Übung 6: Hinzufügen von ActiveX Steuerelementen in InfoPath 2003
  
[Erstellen eines benutzerdefinierten InfoPath-Steuerelements mit C# und .NET (InfoPath-Teamblog)](https://blogs.msdn.microsoft.com/infopath/2005/04/15/creating-an-infopath-custom-control-using-c-and-net/)

