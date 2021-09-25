---
title: Empfangen von Nachrichten mithilfe der benutzerdefinierten TNEF-Anlagenverarbeitung
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: f1706cd14720cf70b83b1cbf1f72d494164a5ca3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578830"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>Empfangen von Nachrichten mithilfe der benutzerdefinierten TNEF-Anlagenverarbeitung

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
So empfangen Sie eine TNEF-Nachricht mit angepasster Anlagenverarbeitung:
  
1. Importieren Sie alle übertragenen Eigenschaften – die vom Messagingsystem unterstützt werden – aus der eingehenden Nachricht in eine neue MAPI-Nachricht. Dazu gehört der Nachrichtentext, der den TNEF-Datenstrom enthält.
    
2. Identifizieren und decodieren Sie die spezielle Anlage, die den TNEF-Stream enthält.
    
3. Extrahieren Sie alle Anlagen aus der eingehenden Nachricht in MAPI-Anlagen der neuen MAPI-Nachricht. Die wiederhergestellten Dateinamen oder andere identifizierende Markierungen in den Anlagen sollten in die **eigenschaft PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) der neuen Anlagen eingefügt werden, damit die [ITnef::ExtractProps-Methode](itnef-extractprops.md) später die richtige Anlage den im Nachrichtentext codierten Anlagentags zuordnen kann. 
    
4. Erstellen Sie eine OLE **IStream-Schnittstelle,** um den decodierten TNEF-Datenstrom zu umschließen und dieses Objekt zusammen mit der neuen MAPI-Nachricht in einem Aufruf der [OpenTnefStreamEx-Funktion](opentnefstreamex.md) zu verwenden. 
    
5. Rufen Sie die **ITnef::ExtractProps-Methode** auf, um die nichttransmittablen Eigenschaften der Nachricht aus dem TNEF-Datenstrom wiederherzustellen. 
    
6. Rufen Sie die [ITnef::OpenTaggedBody-Methode](itnef-opentaggedbody.md) auf, wobei die MAPI_CREATE und MAPI_MODIFY Flags festgelegt sind. Dieser Aufruf entfernt die Anlagentags aus dem Nachrichtentext und konvertiert sie in Anlagenpositionsinformationen in der MAPI-Nachricht. 
    
7. Übermitteln Sie die Nachricht über den MAPI-Spooler.
    

