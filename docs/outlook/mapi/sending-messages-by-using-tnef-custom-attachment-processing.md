---
title: Senden von Nachrichten mit der benutzerdefinierten TNEF-Anlagenverarbeitung
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 1dae8d3a7830ddbc50176ec09415457ca9fdac23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795481"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a>Senden von Nachrichten mit der benutzerdefinierten TNEF-Anlagenverarbeitung

 
  
**Betrifft**: Outlook 
  
So passen Sie Anlage Verarbeitung beim Senden einer Nachricht an
  
1. Abrufen eines TNEF-Objekts, indem Sie eine **IStream** -Schnittstelle und eine Nachricht an die Funktion [OpenTnefStreamEx](opentnefstreamex.md) übergeben. 
    
2. Erhalten Sie eine Liste aller definierten Eigenschaften für die Nachricht, durch die [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode aufrufen. 
    
3. Verwenden Sie [IMAPIProp](imapipropiunknown.md) Methoden, um alle Eigenschaften von messaging-System unterstützt auszuschließen. Schreiben Sie zu einem geeigneten Zeitpunkt diese Eigenschaften in der messaging-System im Format von messaging-System erforderlich. 
    
4. Rufen Sie die [ITnef::AddProps](itnef-addprops.md) -Methode, um nur die Eigenschaften für die Nachricht hinzufügen – d. h., keine der Eigenschaften auf die Anlagen – durch das TNEF_PROP_MESSAGE_ONLY-Flag festlegen. 
    
5. Rufen Sie [ITnef::AddProps](itnef-addprops.md) mit dieser Elemente: das Flag TNEF_PROP_EXCLUDE, einer Array-Eigenschaft Tag mit dem **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) oder **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) Eigenschaft und einer Anlage-ID, der die Anlage zu verarbeitenden angibt.
    
6. Verwenden Sie die [ITnef::SetProps](itnef-setprops.md) -Methode hinzu, die die Anlage an die messaging-System gibt an, ob die Anlage ein Dateinamens hat das **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) Eigenschafts-Tag durch eine eindeutige Zeichenfolge, die die Messaging-System unterstützt nicht. Beispielsweise mehrere Anlagen mit dem gleichen ursprünglichen Dateinamen oder einen Dateinamen ein, der kein gültiger Dateiname für die messaging-System ist. Diese Zeichenfolge wird mit einem Schlüssel mit verwendet werden, wenn die Anlage-Tags im markierten Text schreiben, deren Daten eine Anlage zugeordnet. Weitere Informationen finden Sie unter [TNEF-Tagged des Nachrichtentexts](tnef-tagged-message-text.md).
    
7. Wiederholen Sie die **AddProps** und **SetProps** Anrufe für jede Anlage. 
    
8. Rufen Sie die [ITnef::Finish](itnef-finish.md) -Methode, um die Nachricht in der TNEF-Stream codieren, nachdem alle angeforderten Eigenschaften hinzugefügt werden. 
    
9. Aufrufen der [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) -Methode den markierten Nachrichtentext zu erhalten. Dieser markierte Text wird mithilfe der Methoden aus der **IStream** -Schnittstelle, mit der messaging-System Anlage Modell codiert und in die messaging-System geschrieben gelesen. 
    
10. Rufen Sie die [IUnknown](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode, um das Objekt [ITnef](itnefiunknown.md) freizugeben. 
    
11. Schreiben Sie die verbleibenden Anlagen auf die messaging-System über die messaging-System Anlage Objektmodell.
    
Der Transportdienst sollten das oben beschriebene Verfahren auf Anlagen Prozess verwenden. Wenn dies nicht möglich ist, sollte der Adressbuchhierarchie für angepasste Anlage Verarbeitung die folgenden Schritte verwenden:
  
1. Der Transportdienst wird sichergestellt, dass die **PR_ATTACH_TRANSPORT_NAME** Eigenschaften aller Anlagen eindeutige Werte enthalten, die gültige Anlage Bezeichner für die messaging-System sind. 
    
2. Der Adressbuchhierarchie verwendet einen einzigen Anruf zu **ITnef::AddProps** für jede Anlage, die in das Flag TNEF_PROP_CONTAINED übergeben. 
    

