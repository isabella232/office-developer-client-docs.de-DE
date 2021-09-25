---
title: Öffnen eines Adressbuchcontainers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: df60faa4d28ffbca8fa87c8061c211b219168eda
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600722"
---
# <a name="opening-an-address-book-container"></a>Öffnen eines Adressbuchcontainers

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnen Sie nach dem Öffnen des integrierten MAPI-Adressbuchs einen oder mehrere Adressbuchcontainer, um auf die darin enthaltenen Empfänger zuzugreifen.
  
Um den Container der obersten Ebene des Adressbuchs zu öffnen, rufen [Sie IAddrBook::OpenEntry](iaddrbook-openentry.md) mit einem NULL-Eintragsbezeichner auf. 
  
Adressbuchcontainer können mit Schreibschutz oder Lese-/Schreibzugriff implementiert werden. Schreibgeschützte Container werden nur zum Browsen verwendet. Lese-/Schreibcontainer können geändert werden, sodass Clients neue Einträge erstellen und vorhandene Einträge löschen und ändern können. Alle PAB-Container (Personal Address Book) werden als Lese-/Schreibcontainer implementiert. 
  
Rufen Sie zum Öffnen eines Containers auf niedrigerer Ebene **OpenEntry** auf, und geben Sie den Eintragsbezeichner des zu öffnenden Containers an. 
  
## <a name="open-the-container-designated-as-the-pab"></a>Öffnen des als PAB angegebenen Containers
  
1. Rufen Sie [IAddrBook::GetPAB](iaddrbook-getpab.md) auf, um den Eintragsbezeichner des PAB abzurufen. 
    
2. Übergeben Sie diesen Eintragsbezeichner an [IAddrBook::OpenEntry](iaddrbook-openentry.md).
    
## <a name="open-a-container-that-is-not-the-pab"></a>Öffnen eines Containers, der nicht das PAB ist
  
1. Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) mit einem NULL-Eintragsbezeichner auf, um den Stammcontainer des Adressbuchs zu öffnen. 
    
2. Rufen Sie die [IMAPIContainer::GetHierarchyTable-Methode](imapicontainer-gethierarchytable.md) des Stammcontainers auf, um die Hierarchietabelle abzurufen – eine Liste aller Container auf oberster Ebene im Adressbuch. 
    
3. Wenn der zu öffnende Container einen bestimmten Typ aufweist:
    
   - Erstellen Sie eine **SPropertyRestriction-Struktur** mit **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) für das Eigenschaftentag, den Containertyp für den Eigenschaftswert und RELOP_EQ für die Beziehung. **PR_DISPLAY_TYPE** können auf viele Werte festgelegt werden, darunter: 
    
   - DT_GLOBAL, um die Hierarchietabelle auf Container zu beschränken, die zur globalen Adressliste gehören.
    
   - DT_LOCAL, um die Tabelle auf Container zu beschränken, die zu einem lokalen Adressbuch gehören.
    
   - DT_MODIFIABLE, um die Tabelle auf Container zu beschränken, die geändert werden können.
    
   - Erstellen Sie eine [SPropTagArray-Struktur,](sproptagarray.md) die **PR_ENTRYID,** **PR_DISPLAY_TYPE** und alle anderen interessanten Spalten enthält. 
    
   - Rufen Sie [HrQueryAllRows auf,](hrqueryallrows.md)und übergeben Sie ihr Eigenschaftseinschränkungs- und Eigenschaftstagarray. **HrQueryAllRows** gibt null oder mehr Zeilen zurück, eine Zeile für jeden Container, der zum angegebenen Typ gehört. Bereiten Sie sich darauf vor, die Rückgabe einer beliebigen Anzahl von Zeilen zu verarbeiten. 
    
   - Rufen Sie **IAddrBook::OpenEntry** mit dem Eintragsbezeichner aus der **PR_ENTRYID** Spalte der Zeile auf, die den container von Interesse darstellt. 
    
4. Wenn der zu öffnende Container zu einem bestimmten Adressbuchanbieter gehört:
    
   - Erstellen Sie eine [SPropertyRestriction-Struktur](spropertyrestriction.md) mit **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) für das Eigenschaftstag, einem anbieterspezifischen Wert für den Eigenschaftswert und RELOP_EQ für die Beziehung. In der Regel ist der anbieterspezifische Wert ein global eindeutiger Bezeichner oder eine GUID. Dieser Wert wird in einer der Headerdateien des Adressbuchanbieters veröffentlicht. 
    
   - Erstellen Sie eine [SPropTagArray-Struktur,](sproptagarray.md) die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS** und andere interessante Spalten enthält. 
    
   - Rufen Sie [HrQueryAllRows auf,](hrqueryallrows.md)und übergeben Sie ihr Eigenschaftseinschränkungs- und Eigenschaftstagarray. **HrQueryAllRows** gibt Nullzeilen zurück, wenn sich der angegebene Adressbuchanbieter nicht im Profil befindet. Es kann eine oder mehrere Zeilen für die Container auf oberster Ebene des Anbieters zurückgeben, je nachdem, wie der Anbieter organisiert ist. 
    
   - Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) mit dem Eintragsbezeichner aus der **PR_ENTRYID** Spalte der Zeile auf, die den container von Interesse darstellt. Wenn der Container, an dem Sie interessiert sind, kein Container auf oberster Ebene ist, suchen Sie den Container auf oberster Ebene, und durchlaufen Sie die Hierarchie. 
    

