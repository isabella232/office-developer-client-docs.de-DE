---
title: Unterstützung für benannte Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 983cbaf4d3523bf1e5370e5ad3119ab8c1490f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795671"
---
# <a name="supporting-named-properties"></a>Unterstützung für benannte Eigenschaften

  
  
**Betrifft**: Outlook 
  
Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Unterstützung für benannte Eigenschaften ist für erforderlich: 
  
- Von adressbuchanbietern implementierte, mit denen Sie Einträge von anderen Anbietern in ihre Container kopiert werden können.
    
- Nachrichtenspeicher Authentifizierungsanbieter an, die zum Erstellen von beliebigen Nachrichtentypen verwendet werden können.
    
Unterstützung für benannte Eigenschaft ist optional für alle anderen Dienstanbieter. Dienstanbieter, die Unterstützung für benannte Eigenschaften müssen Namensbezeichner-Zuordnung in den Methoden [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) implementieren. Clients aufrufen **GetNamesFromIDs** zum Abrufen der entsprechenden Names für einen oder mehrere Eigenschaftenbezeichner im Bereich 0 x 8000 Failover und **GetIDsFromNames** entweder erstellen oder die Bezeichner für einen oder mehrere Namen abgerufen. 
  
Dienstanbieter, die keine Unterstützung für benannte Eigenschaften müssen:
  
- Schlagen Sie Aufrufe von [IMAPIProp::SetProps](imapiprop-setprops.md) Eigenschaften mit Bezeichnern oder größer 0 x 8000 Festlegen des MAPI_E_UNEXPECTED_ID im [SPropProblem](spropproblem.md) -Array zurückgeben. 
    
- Geben Sie die Methoden [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) MAPI_E_NO_SUPPORT zurück. 
    

