---
title: Empfangen von Nachrichten mithilfe von TNEF-Anlage benutzerdefinierte Verarbeitung
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 18fc0983554284355dcdfb301fd41a0161a860fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795367"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>Empfangen von Nachrichten mithilfe von TNEF-Anlage benutzerdefinierte Verarbeitung

 
  
**Betrifft**: Outlook 
  
Um eine TNEF-Nachricht mit Anlage benutzerdefinierte Verarbeitung zu erhalten:
  
1. Importieren Sie alle Übertragungseinehit Eigenschaften – die, die das messaging-System unterstützt – aus der eingehenden Nachricht in eine neue MAPI-Nachricht. Dies umfasst den Nachrichtentext an, der den TNEF-Datenstrom enthält.
    
2. Identifizieren Sie und Decodieren Sie spezielle Anlage, die den TNEF-Stream enthält.
    
3. Extrahieren Sie alle Anlagen aus der eingehenden Nachricht in MAPI-Anlagen für die neue MAPI-Nachricht. Die wiederhergestellten Dateinamen oder andere identifizierende Marker auf die Anlagen platziert werden soll in die **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))-Eigenschaft der neuen Anlagen also, die die [ITnef::ExtractProps](itnef-extractprops.md) -Methode die Anlage-Tags in den Nachrichtentext codiert können später die richtige Anlage zugeordnet werden. 
    
4. Erstellen Sie eine OLE- **IStream** -Schnittstelle zum Umschließen des decodierten TNEF-Streams und verwenden Sie dieses Objekt zusammen mit der neuen MAPI-Nachricht in einem Aufruf der Funktion [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Rufen Sie die **ITnef::ExtractProps** -Methode, um die Nontransmittable-Eigenschaften auf die Nachricht aus der TNEF-Datenstrom wiederherstellen. 
    
6. Rufen Sie die [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) -Methode mit dem MAPI_CREATE ist und MAPI_MODIFY Flags. Dieses Anrufs die Anlage-Tags aus dem Nachrichtentext entfernt und in der Anlage Positionsinformationen in der MAPI-Nachricht konvertiert. 
    
7. Die Nachricht über die MAPI-Warteschlange zu übermitteln.
    

