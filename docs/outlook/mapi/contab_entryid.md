---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a2a204f76b62c8c6bc6d8a4e793c936a0184dc65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424084"
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

## <a name="members"></a>Elemente

 **abFlags**
  
> Eine Bitmaske mit Flags, die Informationen zur Beschreibung des Objekts enthält. Weitere Informationen finden Sie in der Beschreibung des **AbFlags-Felds** einer [ENTRYID-Struktur.](entryid.md) 
    
 **muid**
  
> GUID, die den Speicheranbieter identifiziert.
    
 **ulVersion**
  
> Die Versionsnummer der **CONTAB_ENTRYID** Struktur. Muss auf CONTAB_VERSION. 
    
 **ulType**
  
> Eine ganze Zahl, die den Kontakteintrags-ID-Typ darstellt. Dies muss einer der folgenden Werte sein:
    
|**Name**|**Beschreibung**|
|:-----|:-----|
|CONTAB_USER  <br/> |Ein Nachrichtenbenutzer-Objekt.  <br/> |
|CONTAB_DISTLIST  <br/> |Verteilung von List-Objekt.  <br/> |
   
 **ulIndex**
  
> Der Index in die Teilmenge der E-Mail-Eigenschaft.
    
 **cbeid**
  
> Die Größe der Eintrags-ID der Kontaktnachricht, die diesem Eintrag im Adressbuch kontakte zugeordnet ist.
    
 **abeid**
  
> Der Eintragsbezeichner der Kontaktnachricht, die diesem Eintrag im Adressbuch "Kontakte" zugeordnet ist.
    
## <a name="remarks"></a>Hinweise

Ein Kontakt-Adressbuch ist ein Adressbuch, das alle Kontaktelemente in einem Kontaktordner enthält, die entweder eine E-Mail-Adresse oder eine Faxnummer haben. Jeder Eintrag in einem Adressbuch für Kontakte ist entweder einer E-Mail-Adresse oder einer Faxnummer zugeordnet. Da ein Kontaktelement bis zu drei E-Mail-Adressen und drei Faxnummern haben kann, kann ein Kontaktelement durch bis zu sechs Einträge im entsprechenden Kontaktadressenbuch dargestellt werden.
  
Der Zweck eines Adressbuchs für Kontakte besteht in der Unterstützung von Benutzern, die E-Mail-Nachrichten an Kontakte in einem Kontaktordner adressieren. Der Adressbuchanbieter für Kontakte, der Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützt, wird contab32.dll.
  
Die **CONTAB_ENTRYID** unterstützt eine Teilmenge der Informationen, die in der zugrunde liegenden MAPI-Kontaktnachricht vorhanden sind. Es identifiziert die Kontaktnachricht, der ein bestimmter Kontakt-Adressbucheintrag zugeordnet ist. 
  
Die **Felder cbeid** und **abeid** sind nur gültig, wenn der **ulType-Feldwert** auf CONTAB_DISTLIST oder CONTAB_USER. Wenn der wert des **ulType-Felds** auf CONTAB_ROOT, CONTAB_SUBROOT oder CONTAB_CONTAINER festgelegt ist, sollte stattdessen [DIR_ENTRYID](dir_entryid.md) verwendet werden. 
  
## <a name="see-also"></a>Siehe auch



[DIR_ENTRYID](dir_entryid.md)


[MAPI-Strukturen](mapi-structures.md)

