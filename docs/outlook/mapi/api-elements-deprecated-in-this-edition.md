---
title: In dieser Edition veraltete API-Elemente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: abfe734ad8af436f52fc0308d0cd236078bb47df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436888"
---
# <a name="api-elements-deprecated-in-this-edition"></a>In dieser Edition veraltete API-Elemente

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die folgenden API-Elemente sind in der Microsoft Outlook 2013. Sie werden nicht mehr unterstützt, und Sie sollten sie nicht in neuen Projekten verwenden.
  
## <a name="deprecation-of-message-and-recipient-options"></a>Veraltete Nachrichten- und Empfängeroptionen

Die folgenden API-Elemente sind in dieser Version aufgrund veralteter Nachrichten- und Empfängeroptionen veraltet:
  
- **IXPLogon::RegisterOptions**– Das MAPI-Subsystem ruft diese Methode nicht mehr auf, um Standardwerte für Nachrichten- und Empfängeroptionen für einen Transportanbieter zu erstellen.
    
- **OPTIONDATA**– Diese Datenstruktur, die Eigenschaften für Nachrichten- und Empfängeroptionen unterstützt, ist veraltet. Das MAPI-Subsystem ruft **IXPLogon::RegisterOptions** nicht mehr auf, um Nachrichten- oder Empfängeroptionen zu erhalten, die ein Transportanbieter für einen bestimmten Adresstyp unterstützt. 
    
- **OPTIONCALLBACK**– Dieser Funktionsprototyp, den ein Transportanbieter zum Deklarieren einer Rückruffunktion verwendet hat und der wiederum das ZUM Auflösen der Eigenschaften des Anbieters verwendete MAPI-Subsystem ist veraltet. Das MAPI-Subsystem ruft nicht mehr **IXPLogon::RegisterOptions auf** oder verwendet eine rückruffunktion, die vom Transportanbieter zurückgegeben wird. 
    
- **IMAPISession::MessageOptions**– MAPI-Client- und -Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften anzuzeigen oder Benutzern das Festlegen von Eigenschaften zu ermöglichen, die einen bestimmten Nachrichten- und Adresstyp steuern. Die Methode gibt immer MAPI_E_NOT_FOUND zurück, was angibt, dass es keine Nachrichtenoptionen für die bestimmte Nachricht gibt.
    
- **IMAPISession::QueryDefaultMessageOpt**– MAPI-Client- und -Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften abzurufen, die Nachrichtenoptionen für einen bestimmten Adresstyp steuern. Die Methode gibt keinen Zeiger mehr auf ein Array von Eigenschaftswerten zurück.
    
- **IAddrBook::RecipOptions**– MAPI-Client- und -Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften anzuzeigen oder Benutzern das Festlegen von Eigenschaften zu ermöglichen, die die Verarbeitung für einen Empfänger eines bestimmten Adresstyps steuern. Die Methode gibt immer MAPI_W_ERRORS_RETURNED zurück, was angibt, dass es keine Empfängeroptionen für den jeweiligen Empfänger gibt.
    
- **IAddrBook::QueryDefaultRecipOpt**– MAPI-Client- und -Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften abzurufen, die Empfängeroptionen für einen bestimmten Adresstyp steuern. Die Methode gibt keinen Zeiger mehr auf ein Array von Eigenschaftswerten zurück.
    
## <a name="see-also"></a>Siehe auch



[Erste Schritte mit der Outlook-MAPI-Referenz](getting-started-with-the-outlook-mapi-reference.md)

