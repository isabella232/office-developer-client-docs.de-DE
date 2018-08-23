---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d6f5a0bd5da851c5107b8d3d40d683a7e3c1b26b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586011"
---
# <a name="hropenabentrywithprovideruidsupport"></a>HrOpenABEntryWithProviderUIDSupport

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Führt die gleiche Funktion wie die [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) -Funktion, mit der Ausnahme, dass die **HrOpenABEntryWithProviderUIDSupport** -Funktion den Eintrag mithilfe des angegebenen Support-Objekts statt der Sitzung und das Adressbuch wird geöffnet. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUIDSupport(
  const MAPIUID *pEmsabpUID,
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameter

 _pEmsabpUID_
  
> [in] Ein Zeiger auf ein _EmsabpUID_ -Parameter, der die Exchange-Adressbuchanbieter identifiziert, die diese Funktion zum Anzeigen von Details auf die Eintrags-ID verwendet werden soll. Wenn eingehende Eintrags-ID nicht um ein Exchange Address Book Anbieter Eintrags-ID ist, dieser Parameter wird ignoriert, und die Funktion Anruf-verhält sich genau wie [IAddrBook::Details](iaddrbook-details.md). Wenn dieser Parameter auf NULL oder eine MAPIUID NULL ist, verhält sich diese Funktion auch genau wie [IAddrBook::Details](iaddrbook-details.md).
    
 _lpSup_
  
> 
    
 _cbEntryID_
  
> [in] Die Byteanzahl des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID) der Schnittstelle, greifen Sie auf den Eintrag open verwendet werden soll. Übergeben von NULL gibt die standard-Schnittstelle des Objekts zurück. Für die messaging-Benutzer ist der standard-Benutzeroberfläche [IMailUser: IMAPIProp](imailuserimapiprop.md). Wird für es Verteilerlisten [IDistList: IMAPIContainer](idistlistimapicontainer.md), und für Container ist [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Anrufer können auf die entsprechende standard-Schnittstelle oder eine Schnittstelle in der Vererbungshierarchie _LpInterface_ festlegen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ des Texts für den Parameter _LpszButtonText_ steuert. Die folgenden Kennzeichen können festgelegt werden: 
    
AB_TELL_DETAILS_CHANGE
  
> Gibt an, dass Details gibt TRUE zurück, wenn die Adresse tatsächlich geändert werden. Details andernfalls FALSE.
    
DIALOG_MODAL
  
> Zeigt die modale Version im Dialogfeld allgemeine Adresse. Dieses Kennzeichen ist mit DIALOG_SDI gegenseitig aus.
    
DIALOG_SDI
  
> Zeigt die allgemeine Adresse im Dialogfeld ohne Modus Version. Dieses Kennzeichen ist mit DIALOG_MODAL gegenseitig aus.
    
PARAMETER MAPI_UNICODE
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des Eintrags geöffnet.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger des Eintrags geöffnet.
    

