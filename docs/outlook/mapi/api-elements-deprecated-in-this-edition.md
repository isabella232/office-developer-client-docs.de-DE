---
title: In dieser Edition deprecated API-Elemente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: abfe734ad8af436f52fc0308d0cd236078bb47df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318207"
---
# <a name="api-elements-deprecated-in-this-edition"></a>In dieser Edition deprecated API-Elemente

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die folgenden API-Elemente sind in Microsoft Outlook 2013 veraltet. Sie werden nicht mehr unterstützt, und Sie sollten Sie nicht in neuen Projekten verwenden.
  
## <a name="deprecation-of-message-and-recipient-options"></a>Veraltet Nachrichten-und Empfängeroptionen

Die folgenden API-Elemente sind in dieser Release aufgrund veralteter Nachrichten-und Empfängeroptionen veraltet:
  
- **IXPLogon:: Register**Options – das MAPI-Subsystem ruft diese Methode nicht mehr auf, um Standardwerte für Nachrichten-und Empfängeroptionen für einen Transportanbieter einzurichten.
    
- **, OptionDatenquelle**– diese Datenstruktur, die Eigenschaften für Nachrichten-und Empfängeroptionen unterstützt hat, ist veraltet. Das MAPI-Subsystem ruft **IXPLogon:: Register** options nicht mehr auf, um Nachrichten-oder Empfängeroptionen abzurufen, die ein Transportanbieter für einen bestimmten Adresstyp unterstützt. 
    
- **OPTIONCALLBACK**– dieser Funktionsprototyp, den ein Transportanbieter zum Deklarieren einer Rückruffunktion verwendet hat und der wiederum das MAPI-Subsystem zum Auflösen der Eigenschaften des Anbieters verwendet, ist veraltet. Das MAPI-Subsystem ruft **IXPLogon:: registeroptions** nicht mehr auf oder verwendet eine Rückruffunktion, die vom Transportanbieter zurückgegeben wird. 
    
- **IMAPISession:: messageoptions**– MAPI-Client-und-Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften anzuzeigen oder Benutzereigenschaften festzulegen, die eine bestimmte Nachricht und einen bestimmten Adresstyp steuern. Die Methode gibt immer MAPI_E_NOT_FOUND zurück, was bedeutet, dass für die jeweilige Nachricht keine Nachrichtenoptionen vorhanden sind.
    
- **IMAPISession:: QueryDefaultMessageOpt**– MAPI-Client-und-Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften abzurufen, die Nachrichtenoptionen für einen bestimmten Adresstyp steuern. Die-Methode gibt keinen Zeiger mehr auf ein Array von Eigenschaftswerten zurück.
    
- **IAddrBook:: RecipOptions**– MAPI-Client-und-Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften anzuzeigen oder Benutzereigenschaften festzulegen, die die Verarbeitung für einen Empfänger eines bestimmten Adresstyps steuern. Die Methode gibt immer MAPI_W_ERRORS_RETURNED zurück, was bedeutet, dass für den jeweiligen Empfänger keine Empfängeroptionen vorhanden sind.
    
- **IAddrBook:: QueryDefaultRecipOpt**– MAPI-Client-und-Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften abzurufen, die Empfängeroptionen für einen bestimmten Adresstyp steuern. Die-Methode gibt keinen Zeiger mehr auf ein Array von Eigenschaftswerten zurück.
    
## <a name="see-also"></a>Siehe auch



[Erste Schritte mit der Outlook-MAPI-Referenz](getting-started-with-the-outlook-mapi-reference.md)

