---
title: Öffnen eines Adressbuchcontainers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Zuletzt geändert: 20 November, 2011'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326579"
---
# <a name="opening-an-address-book-container"></a>Öffnen eines Adressbuchcontainers

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnen Sie nach dem Öffnen des integrierten MAPI-Adressbuchs einen oder mehrere Adressbuchcontainer für den Zugriff auf die Empfänger in diesen.
  
Um den Container der obersten Ebene des Adressbuchs zu öffnen, rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md) mit einer NULL-Eintrags-ID auf. 
  
Adressbuchcontainer können mit Schreibschutz oder Lese-/Schreibzugriff implementiert werden. Schreibgeschützte Container werden nur zum Browsen verwendet. Container mit Lese-/Schreibzugriff können geändert werden, sodass Clients neue Einträge erstellen und vorhandene Einträge löschen und ändern kann. Alle PAB-Container (persönliches Adressbuch) werden als Lese-/Schreibzugriff-Container implementiert. 
  
Um einen Container mit niedrigerer Ebene zu **** öffnen, rufen Sie OpenEntry auf, und geben Sie den Eintragsbezeichner des zu öffnenden Containers an. 
  
## <a name="open-the-container-designated-as-the-pab"></a>Öffnen des als PAB festgelegten Containers
  
1. Rufen Sie [IAddrBook:: GetPAB](iaddrbook-getpab.md) auf, um die Eintrags-ID des PAB abzurufen. 
    
2. Führen Sie diesen Eintragsbezeichner an [IAddrBook:: OpenEntry](iaddrbook-openentry.md).
    
## <a name="open-a-container-that-is-not-the-pab"></a>Öffnen eines Containers, der nicht das PAB ist
  
1. Rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md) mit einer NULL-Eintrags-ID auf, um den Stammcontainer des Adressbuchs zu öffnen. 
    
2. Rufen Sie die [IMAPIContainer:: gethierarchyid](imapicontainer-gethierarchytable.md) -Methode des Stammcontainers auf, um die Hierarchietabelle abzurufen – eine Liste aller Container der obersten Ebene im Adressbuch. 
    
3. Wenn der Container, der geöffnet werden soll, einen bestimmten Typ hat:
    
   - Erstellen Sie eine **SPropertyRestriction** -Struktur mit **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) für das Property-Tag, den Typ des Containers für den Eigenschaftswert und RELOP_EQ für die Beziehung. **PR_DISPLAY_TYPE** kann auf viele Werte festgelegt werden, darunter: 
    
   - DT_GLOBAL, um die Hierarchietabelle auf Container zu begrenzen, die in die globale Adressliste gehören.
    
   - DT_LOCAL, um die Tabelle auf Container zu begrenzen, die zu einem lokalen Adressbuch gehören.
    
   - DT_MODIFIABLE, um die Tabelle auf Container zu begrenzen, die geändert werden können.
    
   - Erstellen Sie eine [SPropTagArray](sproptagarray.md) -Struktur, die **PR_ENTRYID**, **PR_DISPLAY_TYPE**und alle anderen interessierenden Spalten enthält. 
    
   - Rufen Sie [HrQueryAllRows](hrqueryallrows.md)auf, und übergeben Sie Ihre Eigenschaftseinschränkung und das Property-Tag-Array. **HrQueryAllRows** gibt NULL oder mehr Zeilen zurück, eine Zeile für jeden Container, der zum angegebenen Typ gehört. Bereiten Sie die Rückgabe einer beliebigen Anzahl von Zeilen vor. 
    
   - Rufen Sie **IAddrBook:: OpenEntry** mit der Eintrags-ID aus der **PR_ENTRYID** -Spalte der Zeile, die den Container von Interesse darstellt. 
    
4. Wenn der zu öffnende Container zu einem bestimmten Adressbuchanbieter gehört:
    
   - Erstellen Sie eine [SPropertyRestriction](spropertyrestriction.md) -Struktur mit **PR_AB_PROVIDERS** ([pidtagabproviders (](pidtagabproviders-canonical-property.md)) für das Property-Tag, einen anbieterspezifischen Wert für den Eigenschaftswert und RELOP_EQ für die Beziehung. Der anbieterspezifische Wert ist in der Regel ein global eindeutiger Bezeichner oder eine GUID. Dieser Wert wird in einer der Headerdateien des Adressbuch Anbieters veröffentlicht. 
    
   - Erstellen Sie eine [SPropTagArray](sproptagarray.md) -Struktur, die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**und alle anderen interessierenden Spalten enthält. 
    
   - Rufen Sie [HrQueryAllRows](hrqueryallrows.md)auf, und übergeben Sie Ihre Eigenschaftseinschränkung und das Property-Tag-Array. **HrQueryAllRows** gibt keine Zeilen zurück, wenn sich der angegebene Adressbuchanbieter nicht im Profil befindet. Je nachdem, wie der Anbieter organisiert ist, kann er eine oder mehrere Zeilen für die Container der obersten Ebene des Anbieters zurückgeben. 
    
   - Rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md) mit der Eintrags-ID aus der **PR_ENTRYID** -Spalte der Zeile, die den Container von Interesse darstellt. Wenn der Container, an dem Sie interessiert sind, kein Container der obersten Ebene ist, suchen Sie den Container der obersten Ebene, und überqueren Sie die Hierarchie. 
    

