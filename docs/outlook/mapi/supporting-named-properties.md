---
title: Unterstützen benannter Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 27625e913f06e858295351ed62de840ae7789915
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434326"
---
# <a name="supporting-named-properties"></a>Unterstützen benannter Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Unterstützung für benannte Eigenschaften ist erforderlich für: 
  
- Adressbuchanbieter, die das Kopieren von Einträgen anderer Anbieter in ihre Container zulassen.
    
- Nachrichtenspeicheranbieter, die zum Erstellen beliebiger Nachrichtentypen verwendet werden können.
    
Die Unterstützung benannter Eigenschaften ist für alle anderen Dienstanbieter optional. Dienstanbieter, die benannte Eigenschaften unterstützen, müssen die Zuordnung von Namen zu Bezeichnern in den [Methoden IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) implementieren. Clients rufen **GetNamesFromIDs auf,** um die entsprechenden Namen für einen oder mehrere Eigenschaftenbezeichner im bereich über 0x8000 und **GetIDsFromNames** abzurufen, um die Bezeichner für einen oder mehrere Namen zu erstellen oder abzurufen. 
  
Dienstanbieter, die benannte Eigenschaften nicht unterstützen, müssen:
  
- Fehler bei Aufrufen von [IMAPIProp::SetProps](imapiprop-setprops.md) zum Festlegen von Eigenschaften mit bezeichnern 0x8000 oder höher, indem MAPI_E_UNEXPECTED_ID im [SPropProblem-Array](spropproblem.md) zurückgeben. 
    
- Gibt MAPI_E_NO_SUPPORT von den [Methoden IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) zurück. 
    

