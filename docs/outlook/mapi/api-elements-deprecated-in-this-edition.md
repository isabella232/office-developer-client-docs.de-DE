---
title: In dieser Version veraltete API-Elemente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: e40bcbfffc6f149837f4a11351f2bdbbf0dcc524
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571598"
---
# <a name="api-elements-deprecated-in-this-edition"></a>In dieser Version veraltete API-Elemente

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die folgenden API-Elemente sind in Microsoft Outlook 2013 veraltet. Sie werden nicht mehr unterstützt und sollten sie in neuen Projekten nicht verwenden.
  
## <a name="deprecation-of-message-and-recipient-options"></a>Das Verwerfen der Nachricht sowie die Optionen für Empfänger

Die folgenden API-Elemente sind in dieser Version veraltet, da Sie veraltet Nachrichten- und Optionen:
  
- **IXPLogon::RegisterOptions**– das MAPI-Subsystems nicht mehr diese Methode aufgerufen, um alle Standardwerte für Nachrichten und Empfänger Optionen für eine Adressbuchhierarchie herzustellen.
    
- **OPTIONDATENQUELLE**– diese Datenstruktur, die Eigenschaften für die Nachricht und Empfänger unterstützt ist veraltet. MAPI-Subsystems ruft nicht mehr **IXPLogon::RegisterOptions** erhalten alle Nachrichten oder Optionen, die für einen bestimmten Adresstyp ein Transportdienstes unterstützt. 
    
- **OPTIONCALLBACK**– diese Funktionsprototyp ein Transportdienstes verwendet, um eine Callback-Funktion und, die wiederum Deklarieren des MAPI-Subsystems verwendet, um die Eigenschaften des Anbieters, Auflösen veraltet ist. MAPI-Subsystems nicht mehr aufruft **IXPLogon::RegisterOptions** oder eine beliebige der Adressbuchhierarchie zurückgegebene Callback-Funktion verwendet. 
    
- **IMAPISession::MessageOptions**– MAPI-Client und Dienst Anbieter sollte diese Methode, um Eigenschaften anzuzeigen oder Benutzer Eigenschaften festlegen, die eine bestimmte Nachricht und Adresse Art steuern können nicht mehr aufrufen. Die Methode gibt immer MAPI_E_NOT_FOUND, die angibt, dass keine Nachrichtenoptionen für bestimmte Nachricht vorhanden sind.
    
- **IMAPISession::QueryDefaultMessageOpt**– MAPI-Client und Dienst Anbieter sollte nicht mehr Aufrufen dieser Methode zum Abrufen von Eigenschaften, die für einen bestimmten Adresstyp Nachrichtenoptionen steuern. Die Methode gibt einen Zeiger nicht mehr auf ein Array von Eigenschaftswerten.
    
- **IAddrBook::RecipOptions**– MAPI-Client und Dienst Anbieter sollte diese Methode, um Eigenschaften anzuzeigen, oder lassen Benutzer legen Sie Eigenschaften, die diese Steuerelement Verarbeitung für einen Empfänger, der einen bestimmten Adresstyp nicht mehr aufrufen. Die Methode gibt immer MAPI_W_ERRORS_RETURNED, die angibt, dass es keine Empfänger Optionen für den bestimmten Empfänger sind.
    
- **IAddrBook::QueryDefaultRecipOpt**– MAPI-Client und Dienst Anbieter sollte nicht mehr Aufrufen dieser Methode zum Abrufen von Eigenschaften, die Optionen für einen bestimmten Adresstyp steuern. Die Methode gibt einen Zeiger nicht mehr auf ein Array von Eigenschaftswerten.
    
## <a name="see-also"></a>Siehe auch



[Erste Schritte mit der Outlook-MAPI-Referenz](getting-started-with-the-outlook-mapi-reference.md)

