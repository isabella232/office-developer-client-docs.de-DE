---
title: Senden von Nachrichten mithilfe der benutzerdefinierten TNEF-Anlagenverarbeitung
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
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a>Senden von Nachrichten mithilfe der benutzerdefinierten TNEF-Anlagenverarbeitung

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
So passen Sie die Anlagenverarbeitung beim Senden einer Nachricht an:
  
1. Rufen Sie ein TNEF-Objekt ab, indem Sie eine **IStream-Schnittstelle** und eine Nachricht an die [OpenTnefStreamEx-Funktion](opentnefstreamex.md) übergeben. 
    
2. Rufen Sie eine Liste aller definierten Eigenschaften für die Nachricht ab, indem Sie die [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) aufrufen. 
    
3. Verwenden [Sie IMAPIProp-Methoden,](imapipropiunknown.md) um alle vom Messagingsystem unterstützten Eigenschaften auszuschließen. Schreiben Sie diese Eigenschaften zu einem geeigneten Zeitpunkt in das Messagingsystem im vom Messagingsystem benötigten Format. 
    
4. Rufen Sie die [ITnef::AddProps-Methode](itnef-addprops.md) auf, um nur die Eigenschaften der Nachricht hinzuzufügen, d. h. keine der Eigenschaften für die Anlagen, indem Sie das Flag TNEF_PROP_MESSAGE_ONLY festlegen. 
    
5. Rufen Sie [ITnef::AddProps](itnef-addprops.md) mit diesen Elementen auf: das TNEF_PROP_EXCLUDE-Flag, ein Eigenschaftentagarray, das die **Eigenschaft PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) oder **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) enthält, und einen Anlagenbezeichner, der die zu verarbeitende Anlage angibt.
    
6. Verwenden Sie die [ITnef::SetProps-Methode,](itnef-setprops.md) um das **eigenschaftstag PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) mit einer eindeutigen Zeichenfolge hinzuzufügen, die die Anlage an das Messagingsystem identifiziert, wenn die Anlage einen Dateinamen hat, den das Messagingsystem nicht unterstützen kann. Beispielsweise mehrere Anlagen mit demselben ursprünglichen Dateinamen oder ein Dateiname, der kein gültiger Dateiname für das Messagingsystem ist. Diese Zeichenfolge wird mit einer Schlüsselnummer verwendet, wenn die Anlagentags in den markierten Nachrichtentext geschrieben werden, um eine Anlage ihren Daten zuzuordnen. Weitere Informationen finden Sie unter [TNEF-Tagged Message Text](tnef-tagged-message-text.md).
    
7. Wiederholen Sie **die AddProps-** und **SetProps-Aufrufe** für jede Anlage. 
    
8. Rufen Sie die [ITnef::Finish-Methode](itnef-finish.md) auf, um die Nachricht in den TNEF-Stream zu codieren, nachdem alle angeforderten Eigenschaften hinzugefügt wurden. 
    
9. Rufen Sie den markierten Nachrichtentext ab, indem Sie die [ITnef::OpenTaggedBody-Methode](itnef-opentaggedbody.md) aufrufen. Dieser markierte Text wird mithilfe von Methoden aus der **IStream-Schnittstelle** gelesen, mithilfe des Anlagenmodells des Messagingsystems codiert und in das Messagingsystem geschrieben. 
    
10. Rufen Sie [die IUnknown::Release-Methode auf,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) um das [ITnef-Objekt frei](itnefiunknown.md) zu geben. 
    
11. Schreiben Sie die verbleibenden Anlagen über das Anlagenmodell des Messagingsystems in das Messagingsystem.
    
Ihr Transportanbieter sollte das zuvor beschriebene Verfahren verwenden, um Anlagen zu verarbeiten. Wenn dies nicht möglich ist, sollte der Transportanbieter die folgenden Schritte für die angepasste Anlagenverarbeitung verwenden:
  
1. Der Transportanbieter stellt sicher, **PR_ATTACH_TRANSPORT_NAME** Eigenschaften aller Anlagen eindeutige Werte enthalten, die gültige Anlagenbezeichner für das Messagingsystem sind. 
    
2. Der Transportanbieter verwendet dann einen einzelnen Aufruf von **ITnef::AddProps** für jede Anlage und über TNEF_PROP_CONTAINED Flag. 
    

