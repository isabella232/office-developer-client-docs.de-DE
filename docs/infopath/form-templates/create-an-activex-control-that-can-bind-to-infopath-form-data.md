---
title: Erstellen eines ActiveX-Steuerelements, das an InfoPath-Formulardaten gebunden werden kann
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: Sie können ActiveX in InfoPath-Formularen hosten, die im InfoPath-Editor geöffnet werden sollen. Diese Steuerelemente können bereits vorhanden sein (mit einigen Einschränkungen) oder speziell für InfoPath geschrieben werden.
ms.openlocfilehash: 70ac6a16b305403ffa99d8fe840a165913642f57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300189"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a>Erstellen eines ActiveX-Steuerelements, das an InfoPath-Formulardaten gebunden werden kann

Sie können ActiveX in InfoPath-Formularen hosten, die im InfoPath-Editor geöffnet werden sollen. Diese Steuerelemente können bereits vorhanden sein (mit einigen Einschränkungen) oder speziell für InfoPath geschrieben werden.
  
## <a name="write-an-activex-control"></a>Schreiben eines ActiveX-Steuerelements

Wie bei anderen Steuerelementen in InfoPath sollten ActiveX-Steuerelemente vorhandene Com-Schnittstellen (Component Object Model) unterstützen:
  
- **IDispatch**
    
- **IPersistPropertyBag**
    
- **IPersistStreamInit**
    
- **IPropertyPage**
    
- **IObjectSafety**
    
- **IPropertyNotifySink**
    
- **IViewObject**
    
- **IOleObject**
    
- **IOleInPlaceObject**
    
Damit InfoPath Eigenschaften im Dokumentobjektmodell (DOCUMENT Object Model, DOM) zum Zeitpunkt der Änderung im Steuerelement aktualisiert, sollte das Steuerelement die folgenden Schnittstellen implementieren:
  
- **IConnectionPointContainer**
    
- **IEnumConnectionPoints**
    
- **IConnectionPoint**
    
- **IEnumConnections**
    
Darüber hinaus gibt es zwei InfoPath-spezifische COM-Schnittstellen, die eine engere Integration von Steuerelementen ermöglichen:
  
- [IInfoPathControl](https://msdn.microsoft.com/library/bb264625.aspx)
    
- [IInfoPathControlSite](https://msdn.microsoft.com/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a>Hinzufügen eines ActiveX-Steuerelements zur InfoPath-Entwicklungsumgebung

Mit **dem Befehl Benutzerdefinierte**  Steuerelemente hinzufügen oder entfernen im Aufgabenbereich Steuerelemente können Sie den Assistenten zum Hinzufügen benutzerdefinierter Steuerelemente verwenden, **um** ein benutzerdefiniertes Steuerelement hinzuzufügen. Mithilfe des Assistenten können Sie ein bereits registriertes ActiveX auswählen oder zusätzliche benutzerdefinierte Steuerelemente auf dem Marketplace Office finden. Nachdem Sie ein Steuerelement ausgewählt haben, können Sie die folgenden Elemente angeben. 
  
- Angeben einer CAB-Datei zum Installieren des ActiveX-Steuerelements mit der Formularvorlage
    
- Angeben einer Bindungseigenschaft zum Binden an die XML-Daten
    
- Angeben einer Eigenschaft, die zum Aktivieren oder Deaktivieren des Steuerelements als Reaktion auf Regeln oder digitale Signaturen verwendet wird, was beispielsweise hilfreich sein kann, wenn die XML-Daten nicht vorhanden sind oder wenn bedingte Formatierung verwendet wird
    
- Angeben der Datentypbindung
    
> [!NOTE]
> Wenn Sie ein ActiveX entwickeln und es dem  Aufgabenbereich Steuerelemente in InfoPath hinzugefügt haben, können Sie das ActiveX-Steuerelement erst neu erstellen, wenn InfoPath geschlossen wurde. 
  
## <a name="deploy-an-activex-control"></a>Bereitstellen eines ActiveX-Steuerelements

Zum Verteilen eines ActiveX-Steuerelements können Sie ein Installationsprogramm schreiben, mit dem das Steuerelement auf dem Zielcomputer installiert wird, und die Datei "InfoPath Control Template" (ICT) und die CAB-Datei in den Ordner \Users \\<username \> \AppData\Local\Microsoft\InfoPath\Controls kopiert. Beachten Sie, dass jeder Entwickler über die Steuerelemente verfügen sollte, die der InfoPath-Entwurfsumgebung hinzugefügt wurden, wenn zwei oder mehr Entwickler an der Entwicklung von Formularen arbeiten, die ActiveX-Steuerelementen verwenden, oder wenn sie die Eigenschaften der Steuerelemente aus InfoPath nicht ändern können.
  
## <a name="see-also"></a>Siehe auch

Lab 6: Adding ActiveX Controls in InfoPath 2003
  
[Erstellen eines benutzerdefinierten InfoPath-Steuerelements mithilfe C# und .NET (InfoPath-Teamblog)](https://blogs.msdn.microsoft.com/infopath/2005/04/15/creating-an-infopath-custom-control-using-c-and-net/)

