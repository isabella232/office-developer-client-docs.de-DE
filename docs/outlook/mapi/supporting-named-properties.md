---
title: Unterstützen von benannten Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9ee41469914e52295af219428f26854662c9e2f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582246"
---
# <a name="supporting-named-properties"></a>Unterstützen von benannten Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Unterstützung für benannte Eigenschaften ist für erforderlich: 
  
- Von adressbuchanbietern implementierte, mit denen Sie Einträge von anderen Anbietern in ihre Container kopiert werden können.
    
- Nachrichtenspeicher Authentifizierungsanbieter an, die zum Erstellen von beliebigen Nachrichtentypen verwendet werden können.
    
Unterstützung für benannte Eigenschaft ist optional für alle anderen Dienstanbieter. Dienstanbieter, die Unterstützung für benannte Eigenschaften müssen Namensbezeichner-Zuordnung in den Methoden [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) implementieren. Clients aufrufen **GetNamesFromIDs** zum Abrufen der entsprechenden Names für einen oder mehrere Eigenschaftenbezeichner im Bereich 0 x 8000 Failover und **GetIDsFromNames** entweder erstellen oder die Bezeichner für einen oder mehrere Namen abgerufen. 
  
Dienstanbieter, die keine Unterstützung für benannte Eigenschaften müssen:
  
- Schlagen Sie Aufrufe von [IMAPIProp::SetProps](imapiprop-setprops.md) Eigenschaften mit Bezeichnern oder größer 0 x 8000 Festlegen des MAPI_E_UNEXPECTED_ID im [SPropProblem](spropproblem.md) -Array zurückgeben. 
    
- Geben Sie die Methoden [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) MAPI_E_NO_SUPPORT zurück. 
    

