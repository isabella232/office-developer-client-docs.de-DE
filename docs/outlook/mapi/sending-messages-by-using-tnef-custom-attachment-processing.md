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
ms.openlocfilehash: f9d154b26319f5ed72b1abd6aeef307d07a63bda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339697"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a>Senden von Nachrichten mit der benutzerdefinierten TNEF-Anlagenverarbeitung

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
So passen Sie die Anlagenverarbeitung beim Senden einer Nachricht an
  
1. Rufen Sie ein TNEF-Objekt ab, indem Sie eine **IStream** -Schnittstelle und eine Nachricht an die [OpenTnefStreamEx](opentnefstreamex.md) -Funktion übergeben. 
    
2. Rufen Sie eine Liste aller definierten Eigenschaften für die Nachricht ab, indem Sie die [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode aufrufen. 
    
3. Verwenden Sie [IMAPIProp](imapipropiunknown.md) -Methoden, um alle vom Messagingsystem unterstützten Eigenschaften auszuschließen. Schreiben Sie diese Eigenschaften zu einem geeigneten Zeitpunkt im vom Messagingsystem erforderlichen Format in das Messagingsystem. 
    
4. Rufen Sie die [ITnef::](itnef-addprops.md) AddProps-Methode auf, um nur die Eigenschaften der Nachricht hinzuzufügen, also keine der Eigenschaften in den Anlagen, indem Sie das TNEF_PROP_MESSAGE_ONLY-Flag festlegen. 
    
5. Rufen Sie [ITnef::](itnef-addprops.md) AddProps mit diesen Elementen auf: das TNEF_PROP_EXCLUDE-Flag, ein Property-Tag-Array, das die **PR_ATTACH_DATA_BIN** ([pidtagattachdatabinary (](pidtagattachdatabinary-canonical-property.md)) oder **PR_ATTACH_DATA_OBJ** ([pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md)) enthält. -Eigenschaft und eine Anlagen-ID, die die zu verarbeitende Anlage angibt.
    
6. Verwenden Sie die [ITnef::](itnef-setprops.md) SetProps-Methode, um das **PR_ATTACH_TRANSPORT_NAME** ([pidtagattachtransportname (](pidtagattachtransportname-canonical-property.md))-Eigenschaftentag mit einer eindeutigen Zeichenfolge hinzuzufügen, die die Anlage des Messagingsystems identifiziert, wenn die Anlage einen Dateinamen aufweist, den die Messagingsystem kann nicht unterstützt werden. Beispielsweise mehrere Anlagen mit demselben ursprünglichen Dateinamen oder ein Dateiname, der kein gültiger Dateiname für das Messagingsystem ist. Diese Zeichenfolge wird mit einer Schlüsselnummer verwendet, wenn Sie die Anlagen Tags im markierten Nachrichtentext schreiben, um eine Anlage mit Ihren Daten zu verknüpfen. Weitere Informationen finden Sie unter [TNEF-Tagged Nachrichten Text](tnef-tagged-message-text.md).
    
7. Wiederholen **** Sie die AddProps-und SetProps-Aufrufe für jede Anlage. **** 
    
8. Rufen Sie die [ITnef:: Finish](itnef-finish.md) -Methode auf, um die Nachricht in den TNEF-Stream zu codieren, nachdem alle angeforderten Eigenschaften hinzugefügt wurden. 
    
9. Rufen Sie den markierten Nachrichtentext ab, indem Sie die [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) -Methode aufrufen. Dieser markierte Text wird mithilfe von Methoden der **IStream** -Schnittstelle gelesen, mit dem Anlagenmodell des Messagingsystems codiert und an das Messagingsystem geschrieben. 
    
10. Rufen Sie die [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode auf, um das [ITnef](itnefiunknown.md) -Objekt freigegeben. 
    
11. Schreiben Sie die verbleibenden Anlagen über das Anlagenmodell des Messagingsystems an das Messagingsystem.
    
Der Transportanbieter sollte das zuvor beschriebene Verfahren zum Verarbeiten von Anlagen verwenden. Wenn dies nicht möglich ist, sollte der Transportanbieter die folgenden Schritte für die angepasste Anlagenverarbeitung ausführen:
  
1. Der Transportanbieter stellt sicher, dass die **PR_ATTACH_TRANSPORT_NAME** -Eigenschaften aller Anlagen eindeutige Werte enthalten, die gültige Anlagen-IDs für das Messagingsystem sind. 
    
2. Der Transportanbieter verwendet dann einen einzelnen Aufruf von **ITnef::** AddProps für jede Anlage, wobei das TNEF_PROP_CONTAINED-Flag übergeben wird. 
    

