---
title: Unterstützen benannter Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b989517b38f939796db40291c7a0211c8d3f37fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578543"
---
# <a name="supporting-named-properties"></a>Unterstützen benannter Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Unterstützung für benannte Eigenschaften ist für Folgendes erforderlich: 
  
- Adressbuchanbieter, die das Kopieren von Einträgen von anderen Anbietern in ihre Container zulassen.
    
- Nachrichtenspeicheranbieter, die zum Erstellen beliebiger Nachrichtentypen verwendet werden können.
    
Die Unterstützung benannter Eigenschaften ist für alle anderen Dienstanbieter optional. Dienstanbieter, die benannte Eigenschaften unterstützen, müssen die Zuordnung von Namen zu Bezeichnern in den Methoden [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) implementieren. Clients rufen **GetNamesFromIDs** auf, um die entsprechenden Namen für einen oder mehrere Eigenschaftsbezeichner im Bereich über 0x8000 abzurufen, und **GetIDsFromNames,** um die Bezeichner für einen oder mehrere Namen zu erstellen oder abzurufen. 
  
Dienstanbieter, die keine benannten Eigenschaften unterstützen, müssen:
  
- Fehleraufrufe an [IMAPIProp::SetProps,](imapiprop-setprops.md) um Eigenschaften mit Bezeichnern von 0x8000 oder höher festzulegen, indem MAPI_E_UNEXPECTED_ID im [SPropProblem-Array](spropproblem.md) zurückgegeben werden. 
    
- Zurückgeben MAPI_E_NO_SUPPORT aus den Methoden [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . 
    

