---
title: Anzeigen des Dialog Felds "allgemeine Adresse"
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
# <a name="displaying-the-common-address-dialog-box"></a>Anzeigen des Dialog Felds "allgemeine Adresse"

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Dialogfeld MAPI-allgemeine Adresse kann für eine Vielzahl von Adressierungs Aufgaben wie das Erstellen einer Empfängerliste verwendet werden. Um dieses Dialogfeld anzuzeigen, rufen Sie **IAddrBook:: Address**auf. Je nachdem, welche Zahl von Parametern Sie festlegen und wie Sie Sie festlegen, können Sie die Anzeige auf Einträge eines bestimmten Typs von einem bestimmten Container beschränken.
  
 **So begrenzen Sie das Dialogfeld "Adresse" auf die Anzeige von persönlichen Adressbucheinträgen (PAB)**
  
1. Rufen Sie [IAddrBook:: GetPAB](iaddrbook-getpab.md) auf, um den Eintragsbezeichner des PAB abzurufen. 
    
2. Erstellen Sie eine Eigenschaftseinschränkung, die RELOP_EQ für das **RELOP** -Element der [SPropertyRestriction](spropertyrestriction.md) -Struktur verwendet, und entweder **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) oder **PR_AB_PROVIDER_ID** ([pidtagabproviderid (](pidtagabproviderid-canonical-property.md)) als **ulPropTag** -Element. Wenn Sie **PR_ENTRYID**verwenden, müssen Sie die Eintrags-ID von **GetPAB**. Wenn Sie **PR_AB_PROVIDER_ID**verwenden, müssen Sie den in der MSPAB enthaltenen Wert überschreiten. H-Headerdatei. **PR_AB_PROVIDER_ID** ist der eindeutige Bezeichner für das von MAPI entwickelte PAB. 
    
3. Rufen Sie [IAddrBook:: Address](iaddrbook-address.md) mit dem _lpHierRestriction_ -Parameter auf, der auf die Eigenschaftseinschränkung zeigt. 
    

