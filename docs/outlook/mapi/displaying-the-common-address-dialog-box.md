---
title: Anzeigen des Standarddialogfelds für Adressen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 00d1063310aaf1a8948e04d725d7e11418cf986c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592423"
---
# <a name="displaying-the-common-address-dialog-box"></a>Anzeigen des Standarddialogfelds für Adressen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPI-Adresse im allgemeinen Dialogfeld kann für eine Vielzahl von Adressierung Aufgaben wie das Erstellen einer Empfängerliste verwendet werden. Rufen Sie **IAddrBook::Address**, um das Dialogfeld anzuzeigen. Je nachdem, welches der viele Parameter, die Sie festlegen und wie Sie festlegen, können Sie die Anzeige von einem bestimmten Container den Einträgen eines bestimmten Typs einschränken.
  
 **Um das Dialogfeld Adresse zum Anzeigen von persönlichen (PAB) Adressbucheinträge nur zu begrenzen**
  
1. Rufen Sie [IAddrBook::GetPAB](iaddrbook-getpab.md) , um die Eintrags-ID des PAB abzurufen. 
    
2. Erstellen Sie eine eigenschaftseinschränkung, die für die **relop** Mitglied der [SPropertyRestriction](spropertyrestriction.md) -Struktur und entweder **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) oder **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) RELOP_EQ verwendet als die **UlPropTag** Member. Wenn Sie **PR_ENTRYID**verwenden, übergeben Sie die Eintrags-ID von **GetPAB**abgerufen. Wenn Sie **PR_AB_PROVIDER_ID**verwenden, übergeben Sie den Wert in der MSPAB enthalten. H-Headerdatei. **PR_AB_PROVIDER_ID** ist der eindeutige Bezeichner für die PAB durch MAPI vorgesehen. 
    
3. Rufen Sie [IAddrBook::Address](iaddrbook-address.md) mit dem _LpHierRestriction_ -Parameter auf der eigenschaftseinschränkung zeigen. 
    

