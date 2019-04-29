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
# <a name="contabentryid"></a>CONTAB_ENTRYID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Eintrags-ID des Ordners Kontakte.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |msomapiutil. h  <br/> |
   
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
  
> Eine Bitmaske von Flags, die Informationen zur Beschreibung des Objekts bereitstellt. Weitere Informationen finden Sie in der Beschreibung des **abFlags** -Felds einer [Eintrags](entryid.md) -Struktur. 
    
 **muid**
  
> GUID, die den Informationsspeicher Anbieter identifiziert.
    
 **ulVersion**
  
> Die Versionsnummer der **CONTAB_ENTRYID** -Struktur. Muss auf CONTAB_VERSION festgelegt sein. 
    
 **ulType**
  
> Eine ganze Zahl, die den Typ des Kontakteintrags darstellt. Dabei muss es sich um einen der folgenden Werte handeln:
    
|**Name**|**Beschreibung**|
|:-----|:-----|
|CONTAB_USER  <br/> |Ein Nachrichtenbenutzer-Objekt.  <br/> |
|CONTAB_DISTLIST  <br/> |Verteilung von List-Objekt.  <br/> |
   
 **ulIndex**
  
> Der Index in der e-Mail-Eigenschaft-Teilmenge.
    
 **cbeid**
  
> Die Größe der Eintrags-ID der Kontakt Nachricht, die diesem Eintrag im Adressbuchkontakte zugeordnet ist.
    
 **Abeid**
  
> Die Eintrags-ID der Kontakt Nachricht, die diesem Eintrag im Adressbuchkontakte zugeordnet ist.
    
## <a name="remarks"></a>Bemerkungen

Ein Adressbuch für Kontakte ist ein Adressbuch, das alle Kontaktelemente in einem Kontakteordner enthält, die entweder eine e-Mail-Adresse oder eine Faxnummer enthalten. Jeder Eintrag in einem Contacts-Adressbuch ist entweder einer e-Mail-Adresse oder einer Faxnummer zugeordnet. Da ein Kontaktelement bis zu drei e-Mail-Adressen und drei Faxnummern enthalten kann, kann ein Kontaktelement durch bis zu sechs Einträge im entsprechenden Adressbuch für Kontakte dargestellt werden.
  
Der Zweck eines Kontakt Adressbuchs besteht darin, Benutzer zu unterstützen, die e-Mail-Nachrichten an Kontakte in einem Kontakteordner adressieren. Der Adressbuchanbieter für Kontakte, der von Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützt wird, ist contab32. dll.
  
Die **CONTAB_ENTRYID** -Struktur unterstützt eine Teilmenge der Informationen, die in der zugrunde liegenden MAPI-Kontakt Nachricht enthalten sind. Sie identifiziert die Kontakt Nachricht, der ein bestimmter Adressbucheintrag für Kontakte zugeordnet ist. 
  
Die Felder **cbeid** und **Abeid** sind nur gültig, wenn der **ulType** -Feldwert auf CONTAB_DISTLIST oder CONTAB_USER festgelegt ist. Wenn der **ulType** -FELDWERT auf CONTAB_ROOT, CONTAB_SUBROOT oder CONTAB_CONTAINER festgelegt ist, sollte stattdessen die [DIR_ENTRYID](dir_entryid.md) -Struktur verwendet werden. 
  
## <a name="see-also"></a>Siehe auch



[DIR_ENTRYID](dir_entryid.md)


[MAPI-Strukturen](mapi-structures.md)

