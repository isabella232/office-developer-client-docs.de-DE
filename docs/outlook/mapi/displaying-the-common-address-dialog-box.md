---
title: Anzeigen des allgemeinen Adressdialogfelds
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 81264e5cbf84bf4b8dcbed6ab31c7909fa04483d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596575"
---
# <a name="displaying-the-common-address-dialog-box"></a>Anzeigen des allgemeinen Adressdialogfelds

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das allgemeine MapI-Adressdialogfeld kann für eine Vielzahl von Adressierungsaufgaben wie das Erstellen einer Empfängerliste verwendet werden. Rufen Sie **IAddrBook::Address** auf, um dieses Dialogfeld anzuzeigen. Je nachdem, welche der vielen Parameter Sie festlegen und wie Sie sie festlegen, können Sie die Anzeige auf Einträge eines bestimmten Typs aus einem bestimmten Container beschränken.
  
 **So beschränken Sie das Adressdialogfeld auf die Anzeige von PAB-Einträgen (Personal Address Book)**
  
1. Rufen Sie [IAddrBook::GetPAB](iaddrbook-getpab.md) auf, um den Eintragsbezeichner des PAB abzurufen. 
    
2. Erstellen Sie eine Eigenschaftseinschränkung, die RELOP_EQ für das **Relop-Element** der [SPropertyRestriction-Struktur](spropertyrestriction.md) und entweder **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) oder **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) als **ulPropTag-Element** verwendet. Wenn Sie **PR_ENTRYID** verwenden, übergeben Sie den aus **GetPAB** abgerufenen Eintragsbezeichner. Wenn Sie **PR_AB_PROVIDER_ID** verwenden, übergeben Sie den im MSPAB enthaltenen Wert. H-Headerdatei. **PR_AB_PROVIDER_ID** ist der eindeutige Bezeichner für das von mapi entworfene PAB. 
    
3. Rufen Sie [IAddrBook::Address](iaddrbook-address.md) auf, wobei der  _parameter lpHierRestriction_ auf die Eigenschaftseinschränkung verweist. 
    

