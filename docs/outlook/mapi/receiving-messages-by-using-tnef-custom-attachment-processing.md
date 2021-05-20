---
title: Empfangen von Nachrichten mithilfe der benutzerdefinierten TNEF-Anlagenverarbeitung
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 046b537d41b318fa857ef77f1906edcf2c3aa2bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429320"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>Empfangen von Nachrichten mithilfe der benutzerdefinierten TNEF-Anlagenverarbeitung

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
So empfangen Sie eine TNEF-Nachricht mit angepasster Anlagenverarbeitung:
  
1. Importieren Sie alle übertragungsbaren Eigenschaften , die vom Messagingsystem unterstützt werden, aus der eingehenden Nachricht in eine neue MAPI-Nachricht. Dies umfasst den Nachrichtentext, der den TNEF-Datenstrom enthält.
    
2. Identifizieren und decodieren Sie die spezielle Anlage, die den TNEF-Stream enthält.
    
3. Extrahieren Sie alle Anlagen aus der eingehenden Nachricht in MAPI-Anlagen in der neuen MAPI-Nachricht. Die wiederhergestellten Dateinamen oder andere identifizierende Markierungen für die Anlagen sollten in der **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))-Eigenschaft der neuen Anlagen platziert werden, damit die [ITnef::ExtractProps-Methode](itnef-extractprops.md) später die richtige Anlage den im Nachrichtentext codierten Anlagentags zuordnen kann. 
    
4. Erstellen Sie eine OLE **IStream-Schnittstelle,** um den decodierten TNEF-Stream zu umschließen, und verwenden Sie dieses Objekt zusammen mit der neuen MAPI-Nachricht in einem Aufruf der [OpenTnefStreamEx-Funktion.](opentnefstreamex.md) 
    
5. Rufen Sie **die ITnef::ExtractProps-Methode** auf, um die nichttransmittablen Eigenschaften der Nachricht aus dem TNEF-Datenstrom wiederhergestellt zu werden. 
    
6. Rufen Sie [die ITnef::OpenTaggedBody-Methode](itnef-opentaggedbody.md) auf, MAPI_CREATE und MAPI_MODIFY festgelegt sind. Mit diesem Aufruf werden die Anlagentags aus dem Nachrichtentext entfernt und in Anlagenpositionsinformationen in der MAPI-Nachricht konvertiert. 
    
7. Senden Sie die Nachricht über den MAPI-Spooler.
    

