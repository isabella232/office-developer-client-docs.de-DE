---
title: Senden von Nachrichten mithilfe der benutzerdefinierten TNEF-Anlagenverarbeitung
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 1456cd4d949799862c9d07cb3f733810bdc409c2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578669"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a>Senden von Nachrichten mithilfe der benutzerdefinierten TNEF-Anlagenverarbeitung

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
So passen Sie die Anlagenverarbeitung beim Senden einer Nachricht an:
  
1. Rufen Sie ein TNEF-Objekt ab, indem Sie eine **IStream-Schnittstelle** und eine Nachricht an die [OpenTnefStreamEx-Funktion](opentnefstreamex.md) übergeben. 
    
2. Rufen Sie eine Liste aller definierten Eigenschaften für die Nachricht ab, indem Sie die [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) aufrufen. 
    
3. Verwenden Sie [IMAPIProp-Methoden,](imapipropiunknown.md) um alle vom Messagingsystem unterstützten Eigenschaften auszuschließen. Schreiben Sie diese Eigenschaften zu einem geeigneten Zeitpunkt in das Messagingsystem in dem vom Messagingsystem erforderlichen Format. 
    
4. Rufen Sie die [ITnef::AddProps-Methode](itnef-addprops.md) auf, um nur die Eigenschaften der Nachricht hinzuzufügen , d. h. keine der Eigenschaften in den Anlagen, indem Sie das TNEF_PROP_MESSAGE_ONLY-Kennzeichen festlegen. 
    
5. Rufen Sie [ITnef::AddProps](itnef-addprops.md) mit diesen Elementen auf: das TNEF_PROP_EXCLUDE-Flag, ein Eigenschaftentagarray, das die **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) oder **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) -Eigenschaft enthält, und einen Anlagenbezeichner, der die zu verarbeitende Anlage angibt.
    
6. Verwenden Sie die [ITnef::SetProps-Methode,](itnef-setprops.md) um das **Eigenschaftentag PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) mit einer eindeutigen Zeichenfolge hinzuzufügen, die die Anlage an das Messagingsystem identifiziert, wenn die Anlage einen Dateinamen aufweist, den das Messagingsystem nicht unterstützen kann. Beispielsweise mehrere Anlagen mit demselben ursprünglichen Dateinamen oder einen Dateinamen, der kein gültiger Dateiname für das Messagingsystem ist. Diese Zeichenfolge wird mit einer Schlüsselnummer verwendet, wenn die Anlagentags im markierten Nachrichtentext geschrieben werden, um eine Anlage ihren Daten zuzuordnen. Weitere Informationen finden Sie unter [TNEF-Tagged Message Text](tnef-tagged-message-text.md).
    
7. Wiederholen Sie die **AddProps-** und **SetProps-Aufrufe** für jede Anlage. 
    
8. Rufen Sie die [ITnef::Finish-Methode](itnef-finish.md) auf, um die Nachricht im TNEF-Stream zu codieren, nachdem alle angeforderten Eigenschaften hinzugefügt wurden. 
    
9. Rufen Sie den markierten Nachrichtentext ab, indem Sie die [ITnef::OpenTaggedBody-Methode](itnef-opentaggedbody.md) aufrufen. Dieser markierte Text wird mithilfe von Methoden aus der **IStream-Schnittstelle** gelesen, mithilfe des Anlagenmodells des Messagingsystems codiert und in das Messagingsystem geschrieben. 
    
10. Rufen Sie die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) auf, um das [ITnef-Objekt](itnefiunknown.md) freizugeben. 
    
11. Schreiben Sie die verbleibenden Anlagen über das Anlagenmodell des Messagingsystems in das Messagingsystem.
    
Ihr Transportanbieter sollte das zuvor beschriebene Verfahren zum Verarbeiten von Anlagen verwenden. Wenn dies nicht möglich ist, sollte der Transportanbieter die folgenden Schritte für die benutzerdefinierte Anlagenverarbeitung verwenden:
  
1. Der Transportanbieter stellt sicher, dass die **PR_ATTACH_TRANSPORT_NAME** Eigenschaften aller Anlagen eindeutige Werte enthalten, die gültige Anlagenbezeichner für das Messagingsystem sind. 
    
2. Der Transportanbieter verwendet dann einen einzelnen Aufruf von **ITnef::AddProps** für jede Anlage, wobei das TNEF_PROP_CONTAINED Flag übergeben wird. 
    

