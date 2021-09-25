---
title: In dieser Edition veraltete API-Elemente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: ad61750e5b194859e4ed2b8963d017f3cabfb414
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588231"
---
# <a name="api-elements-deprecated-in-this-edition"></a>In dieser Edition veraltete API-Elemente

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die folgenden API-Elemente sind in Microsoft Outlook 2013 veraltet. Sie werden nicht mehr unterstützt, und Sie sollten sie nicht in neuen Projekten verwenden.
  
## <a name="deprecation-of-message-and-recipient-options"></a>Veraltete Nachrichten- und Empfängeroptionen

Die folgenden API-Elemente sind in dieser Version aufgrund veralteter Nachrichten- und Empfängeroptionen veraltet:
  
- **IXPLogon::RegisterOptions**- Das MAPI-Subsystem ruft diese Methode nicht mehr auf, um Standardwerte für Nachrichten- und Empfängeroptionen für einen Transportanbieter festzulegen.
    
- **OPTIONDATA**– Diese Datenstruktur, die Eigenschaften für Nachrichten- und Empfängeroptionen unterstützt, ist veraltet. Das MAPI-Subsystem ruft **IXPLogon::RegisterOptions** nicht mehr auf, um Nachrichten- oder Empfängeroptionen abzurufen, die ein Transportanbieter für einen bestimmten Adresstyp unterstützt. 
    
- **OPTIONCALLBACK**– Dieser Funktionsprototyp, der von einem Transportanbieter zum Deklarieren einer Rückruffunktion verwendet wurde und mit dem wiederum das MAPI-Subsystem, mit dem die Eigenschaften des Anbieters aufgelöst werden, veraltet ist. Das MAPI-Subsystem ruft **IXPLogon::RegisterOptions** nicht mehr auf oder verwendet keine rückruffunktion, die vom Transportanbieter zurückgegeben wird. 
    
- **IMAPISession::MessageOptions**- MAPI-Client- und -Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften anzuzeigen oder Benutzern das Festlegen von Eigenschaften zu ermöglichen, die eine bestimmte Nachricht und einen bestimmten Adresstyp steuern. Die Methode gibt immer MAPI_E_NOT_FOUND zurück, was bedeutet, dass für die bestimmte Nachricht keine Nachrichtenoptionen vorhanden sind.
    
- **IMAPISession::QueryDefaultMessageOpt**- MAPI-Client- und Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften abzurufen, die Nachrichtenoptionen für einen bestimmten Adresstyp steuern. Die Methode gibt keinen Zeiger mehr auf ein Array von Eigenschaftswerten zurück.
    
- **IAddrBook::RecipOptions**- MAPI-Client und Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften anzuzeigen oder Benutzern das Festlegen von Eigenschaften zu ermöglichen, die die Verarbeitung für einen Empfänger eines bestimmten Adresstyps steuern. Die Methode gibt immer MAPI_W_ERRORS_RETURNED zurück, was bedeutet, dass für den jeweiligen Empfänger keine Empfängeroptionen vorhanden sind.
    
- **IAddrBook::QueryDefaultRecipOpt**- MAPI-Client- und -Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften abzurufen, die Empfängeroptionen für einen bestimmten Adresstyp steuern. Die Methode gibt keinen Zeiger mehr auf ein Array von Eigenschaftswerten zurück.
    
## <a name="see-also"></a>Siehe auch



[Erste Schritte mit der Outlook-MAPI-Referenz](getting-started-with-the-outlook-mapi-reference.md)

