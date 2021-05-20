---
title: Anzeigen des Dialogfelds "Allgemeine Adresse"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 812c850d1fcb6d3712d76b160b56b839b2e1353d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436903"
---
# <a name="displaying-the-common-address-dialog-box"></a>Anzeigen des Dialogfelds "Allgemeine Adresse"

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Dialogfeld allgemeine MAPI-Adresse kann für eine Vielzahl von Adressierungsaufgaben verwendet werden, z. B. das Erstellen einer Empfängerliste. Rufen Sie zum Anzeigen dieses Dialogfelds **IAddrBook::Address auf.** Je nachdem, welche der vielen Parameter Sie festlegen und wie Sie sie festlegen, können Sie die Anzeige auf Einträge eines bestimmten Typs aus einem bestimmten Container beschränken.
  
 **So beschränken Sie das Adressdialogfeld auf die Anzeige von Einträgen im persönlichen Adressbuch (PAB)**
  
1. Rufen [Sie IAddrBook::GetPAB auf,](iaddrbook-getpab.md) um die Eintrags-ID des PAB abzurufen. 
    
2. Erstellen Sie eine Eigenschaftseinschränkung, die RELOP_EQ für das **#A0** der [SPropertyRestriction-Struktur](spropertyrestriction.md) und **entweder PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) oder **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) als **ulPropTag-Element** verwendet. Wenn Sie **PR_ENTRYID** verwenden, übergeben Sie den eintragsbezeichner, der aus **GetPAB abgerufen wurde.** Wenn Sie **PR_AB_PROVIDER_ID** verwenden, übergeben Sie den im MSPAB enthaltenen Wert. H-Headerdatei. **PR_AB_PROVIDER_ID** ist der eindeutige Bezeichner für das von MAPI entworfene PAB. 
    
3. Rufen [Sie IAddrBook::Address auf,](iaddrbook-address.md) mit dem  _lpHierRestriction-Parameter,_ der auf die Eigenschaftseinschränkung verweisen soll. 
    

