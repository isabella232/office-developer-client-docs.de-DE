---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cb6138072cd5dedc528168d4056041661c40fd06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791921"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**Betrifft**: Outlook 
  
Stellt sicher, dass die **OpenEntry** -Methode durch die erwartete Exchange-Adressbuchanbieter geöffnet wird. Diese Funktion verhält sich [IAddrBook::Details](iaddrbook-details.md), jedoch wird die **Eintrags-ID** mithilfe des Exchange-Adressbuchs vom Parameter _pEmsmdbUID_ geöffnet. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithExchangeContext(
  LPMAPISESSION   pmsess,
  const MAPIUID  *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags,
);
```

## <a name="parameters"></a>Parameter

 _pmsess_
  
> Die angemeldete **IMAPISession**. Es darf nicht NULL sein.
    
 _pEmsmdbUID_
  
> Ein Zeiger auf eine **EmsmdbUID** , die den Exchange-Dienst, die die Exchange-Adressbuchanbieter, die von der Funktion verwendet wird identifiziert enthält, um die Eintrags-ID zu öffnen. Wenn eingehende Eintrags-ID kein Exchange Address Book Anbieter Eintrags-ID ist, wird dieser Parameter wird ignoriert, und die Funktion verhält sich wie [IAddrBook::OpenEntry](iaddrbook-openentry.md). Wenn dieser Parameter auf NULL oder NULL **MAPIUID**ist, verhält sich diese Funktion auch genau wie [IAddrBook::OpenEntry](iaddrbook-openentry.md). 
    
 _pAddrBook_
  
> [in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen. Es darf nicht NULL sein.
    
 _lpulUIParam_
  
> [out] Ein Handle für das übergeordnete Fenster für das Dialogfeld.
    
 _lpfnDismiss_
  
> [in] Ein Zeiger auf eine Funktion, die basierend auf dem **DISMISSMODELESS** Prototyp oder NULL. Dieser Member gilt nur für die im Dialogfeld ohne Modus Version durch das DIALOG_SDI-Flag festgelegt wird. MAPI-Aufrufen die **DISMISSMODELESS** -Funktion, wenn der Benutzer schließt das Dialogfeld ohne Modus Adresse informiert einen Client, der Details anruft, dass das Dialogfeld nicht mehr aktiv ist. 
    
 _lpvDismissContext_
  
> [in] Ein Zeiger auf Kontextinformationen zum Übergeben an die Funktion **DISMISSMODELESS** an, durch den Parameter _LpfnDismiss_ auf. Dieser Parameter gilt nur für die im Dialogfeld ohne Modus Version durch das **DIALOG_SDI** -Flag in den Parameter _UlFlags_ einschließen. 
    
 _cbEntryID_
  
> [in] Die Byteanzahl des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt.
    
 _lpfButtonCallback_
  
> [in] Ein Zeiger auf eine Funktion, die basierend auf den **LPFNBUTTON** Funktionsprototyp. Eine **LPFNBUTTON** -Funktion hinzugefügt im Dialogfeld Details der eine Schaltfläche. 
    
 _lpvButtonContext_
  
> [in] Ein Zeiger auf Daten, die als Parameter für die Funktion, die durch den _LpfButtonCallback_ -Parameter angegebenen verwendet wurde. 
    
 _lpszButtonText_
  
> [in] Ein Zeiger auf eine Zeichenfolge mit Text auf die Schaltfläche hinzugefügt, angewendet werden soll, wenn diese Schaltfläche erweiterbar ist. Der Parameter _LpszButtonText_ sollte NULL sein, wenn eine erweiterbare Schaltfläche nicht benötigt wird. 
    
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
    

