---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aa3a232072e535d7db384316edb591ae340a64b5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605097"
---
# <a name="contab_entryid"></a>CONTAB_ENTRYID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Eintrags-ID des Kontaktordners.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |msomapiutil.h  <br/> |
   
```cpp
#pragma pack(4) 
typedef struct _contab_entryid
{
    BYTE abFlags[4];
    MAPIUID muid;
    ULONG ulVersion;
    ULONG ulType;
    ULONG ulIndex;
    ULONG cbeid;
    BYTE abeid[1];
}   CONTAB_ENTRYID, *LPCONTAB_ENTRYID;
#pragma pack() 
```

## <a name="members"></a>Members

 **abFlags**
  
> Eine Bitmaske mit Flags, die Informationen zur Beschreibung des Objekts bereitstellt. Weitere Informationen finden Sie in der Beschreibung des **abFlags-Felds** einer [ENTRYID-Struktur.](entryid.md) 
    
 **muid**
  
> GUID, die den Store-Anbieter identifiziert.
    
 **ulVersion**
  
> Die Versionsnummer der **CONTAB_ENTRYID** Struktur. Muss auf CONTAB_VERSION festgelegt werden. 
    
 **ulType**
  
> Eine ganze Zahl, die den Id-Typ des Kontakteintrags darstellt. Es muss einer der folgenden Werte sein:
    
|**Name**|**Beschreibung**|
|:-----|:-----|
|CONTAB_USER  <br/> |Ein Nachrichtenbenutzer-Objekt.  <br/> |
|CONTAB_DISTLIST  <br/> |Verteilung von List-Objekt.  <br/> |
   
 **ulIndex**
  
> Der Index in der Teilmenge der E-Mail-Eigenschaft.
    
 **cbeid**
  
> Die Größe des Eintragsbezeichners der Kontaktnachricht, die diesem Eintrag im Adressbuch für Kontakte zugeordnet ist.
    
 **abeid**
  
> Der Eintragsbezeichner der Kontaktnachricht, die diesem Eintrag im Adressbuch für Kontakte zugeordnet ist.
    
## <a name="remarks"></a>HinwBemerkungeneise

Ein Kontaktadressbuch ist ein Adressbuch, das alle Kontaktelemente in einem Kontaktordner enthält, die entweder eine E-Mail-Adresse oder eine Faxnummer aufweisen. Jeder Eintrag in einem Kontaktadressbuch ist entweder einer E-Mail-Adresse oder einer Faxnummer zugeordnet. Da ein Kontaktelement bis zu drei E-Mail-Adressen und drei Faxnummern haben kann, kann ein Kontaktelement durch bis zu sechs Einträge im entsprechenden Kontaktadressbuch dargestellt werden.
  
Der Zweck eines Kontaktadressbuchs besteht darin, Benutzer beim Adressieren von E-Mail-Nachrichten an Kontakte in einem Kontaktordner zu unterstützen. Der Adressbuchanbieter für Kontakte, der Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützt, ist contab32.dll.
  
Die **CONTAB_ENTRYID-Struktur** unterstützt eine Teilmenge der Informationen, die in der zugrunde liegenden MAPI-Kontaktnachricht vorhanden sind. Es identifiziert die Kontaktnachricht, der ein bestimmter Kontaktadressbucheintrag zugeordnet ist. 
  
Die **Felder "cbeid"** und **"abeid"** sind nur gültig, wenn der **UlType-Feldwert** auf CONTAB_DISTLIST oder CONTAB_USER festgelegt ist. Wenn der **ulType-Feldwert** auf CONTAB_ROOT, CONTAB_SUBROOT oder CONTAB_CONTAINER festgelegt ist, sollte stattdessen die [DIR_ENTRYID](dir_entryid.md) Struktur verwendet werden. 
  
## <a name="see-also"></a>Siehe auch



[DIR_ENTRYID](dir_entryid.md)


[MAPI-Strukturen](mapi-structures.md)

