---
title: Öffnen eines Adressbuchcontainers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Letzte Änderung: 08. November 2011'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436741"
---
# <a name="opening-an-address-book-container"></a>Öffnen eines Adressbuchcontainers

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnen Sie nach dem Öffnen des integrierten Adressbuchs MAPI einen oder mehrere Adressbuchcontainer, um auf die empfänger in ihnen zu zugreifen.
  
Um den Container auf oberster Ebene des Adressbuchs zu öffnen, rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) mit einem NULL-Eintragsbezeichner auf. 
  
Adressbuchcontainer können mit Lese-/Schreibzugriff implementiert werden. Schreibgeschützte Container werden nur zum Browsen verwendet. Lese-/Schreibzugriffscontainer können geändert werden, sodass Clients neue Einträge erstellen und vorhandene Einträge löschen und ändern können. Alle Persönliche Adressbuchcontainer (PAB) werden als Lese-/Schreibcontainer implementiert. 
  
Rufen Sie **openEntry** auf, und geben Sie den Eintragsbezeichner des zu öffnenden Containers an, um einen Container auf niedrigerer Ebene zu öffnen. 
  
## <a name="open-the-container-designated-as-the-pab"></a>Öffnen des als PAB festgelegten Containers
  
1. Rufen [Sie IAddrBook::GetPAB auf,](iaddrbook-getpab.md) um den Eintragsbezeichner des PAB abzurufen. 
    
2. Übergeben Sie diesen Eintragsbezeichner [an IAddrBook::OpenEntry](iaddrbook-openentry.md).
    
## <a name="open-a-container-that-is-not-the-pab"></a>Öffnen eines Containers, der nicht das PAB ist
  
1. Rufen [Sie IAddrBook::OpenEntry](iaddrbook-openentry.md) mit einem NULL-Eintragsbezeichner auf, um den Stammcontainer des Adressbuchs zu öffnen. 
    
2. Rufen Sie die [IMAPIContainer::GetHierarchyTable-Methode](imapicontainer-gethierarchytable.md) des Stammcontainers auf, um die Hierarchietabelle abzurufen – eine Liste aller Container auf oberster Ebene im Adressbuch. 
    
3. Wenn der zu öffnende Container einen bestimmten Typ hat:
    
   - Erstellen Sie eine **SPropertyRestriction-Struktur** mit **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) für das Eigenschaftstag, den Containertyp für den Eigenschaftswert und RELOP_EQ für die Beziehung. **PR_DISPLAY_TYPE** können auf viele Werte festgelegt werden, darunter: 
    
   - DT_GLOBAL, um die Hierarchietabelle auf Container zu beschränken, die in die globale Adressliste gehören.
    
   - DT_LOCAL, um die Tabelle auf Container zu beschränken, die zu einem lokalen Adressbuch gehören.
    
   - DT_MODIFIABLE, um die Tabelle auf Container zu beschränken, die geändert werden können.
    
   - Erstellen Sie [eine SPropTagArray-Struktur,](sproptagarray.md) die **PR_ENTRYID**, **PR_DISPLAY_TYPE** und andere wichtige Spalten enthält. 
    
   - Rufen [Sie HrQueryAllRows auf,](hrqueryallrows.md)und übergeben Sie ihr Eigenschaftseinschränkungs- und Eigenschaftentagarray. **HrQueryAllRows** gibt null oder mehr Zeilen zurück, eine Zeile für jeden Container, der zum angegebenen Typ gehört. Bereiten Sie sich darauf vor, die Rückgabe einer beliebigen Anzahl von Zeilen zu verarbeiten. 
    
   - Rufen **Sie IAddrBook::OpenEntry** mit dem Eintragsbezeichner aus der spalte **PR_ENTRYID** der Zeile auf, die den container von Interesse darstellt. 
    
4. Wenn der zu öffnende Container zu einem bestimmten Adressbuchanbieter gehört:
    
   - Erstellen Sie eine [SPropertyRestriction-Struktur](spropertyrestriction.md) mit **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) für das Eigenschaftstag, einen anbieterspezifischen Wert für den Eigenschaftswert und RELOP_EQ für die Beziehung. In der Regel ist der anbieterspezifische Wert eine global eindeutige ID oder GUID. Dieser Wert wird in einer der Headerdateien des Adressbuchanbieters veröffentlicht. 
    
   - Erstellen Sie [eine SPropTagArray-Struktur,](sproptagarray.md) die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS** und alle anderen von Interesse eignen Spalten enthält. 
    
   - Rufen [Sie HrQueryAllRows auf,](hrqueryallrows.md)und übergeben Sie ihr Eigenschaftseinschränkungs- und Eigenschaftentagarray. **HrQueryAllRows** gibt null Zeilen zurück, wenn sich der angegebene Adressbuchanbieter nicht im Profil befindet. Je nach Organisation des Anbieters kann eine oder mehrere Zeilen für die Container auf oberster Ebene des Anbieters zurückgegeben werden. 
    
   - Rufen [Sie IAddrBook::OpenEntry](iaddrbook-openentry.md) mit dem Eintragsbezeichner aus der spalte **PR_ENTRYID** der Zeile auf, die den container von Interesse darstellt. Wenn es sich bei dem Container, an dem Sie interessiert sind, nicht um einen Container auf oberster Ebene handelt, suchen Sie den Container auf oberster Ebene, und durchlaufen Sie die Hierarchie. 
    

