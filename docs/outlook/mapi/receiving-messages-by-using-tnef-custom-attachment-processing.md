---
title: Empfangen von Nachrichten mit der benutzerdefinierten TNEF-Anlagenverarbeitung
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
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>Empfangen von Nachrichten mit der benutzerdefinierten TNEF-Anlagenverarbeitung

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
So erhalten Sie eine TNEF-Nachricht mit angepasster Anlagenverarbeitung:
  
1. Importieren Sie alle transmitable-Eigenschaften, die vom Messagingsystem unterstützt werden, von der eingehenden Nachricht in eine neue MAPI-Nachricht. Hierzu gehört der Nachrichtentext, der den TNEF-Datenstrom enthält.
    
2. Identifizieren und Decodieren Sie die spezielle Anlage, die den TNEF-Datenstrom enthält.
    
3. Extrahieren Sie alle Anlagen aus der eingehenden Nachricht in MAPI-Anlagen in der neuen MAPI-Nachricht. Die wiederhergestellten Dateinamen oder anderen identifizierenden Marker für die Anlagen sollten in der **PR_ATTACH_TRANSPORT_NAME** ([pidtagattachtransportname (](pidtagattachtransportname-canonical-property.md))-Eigenschaft der neuen Anlagen platziert werden, damit die [ITnef:: ExtractProps](itnef-extractprops.md) -Methode die richtige Anlage kann später mit den im Nachrichtentext codierten Anlagen Tags verknüpft werden. 
    
4. Erstellen Sie eine OLE **IStream** -Schnittstelle, um den deCODIERTen TNEF-Stream zu umbrechen, und verwenden Sie dieses Objekt zusammen mit der neuen MAPI-Nachricht in einem Aufruf der [OpenTnefStreamEx](opentnefstreamex.md) -Funktion. 
    
5. Rufen Sie die **ITnef:: ExtractProps** -Methode auf, um die nicht übertragbaren Eigenschaften für die Nachricht aus dem TNEF-Datenstrom wiederherzustellen. 
    
6. Rufen Sie die [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) -Methode auf, wobei die Flags MAPI_CREATE und MAPI_MODIFY festgelegt sind. Dieser Aufruf entfernt die Anlagen Tags aus dem Nachrichtentext und wandelt sie in die Informationen zur Anlagen Position in der MAPI-Nachricht um. 
    
7. Übermitteln Sie die Nachricht über den MAPI-Spooler.
    

