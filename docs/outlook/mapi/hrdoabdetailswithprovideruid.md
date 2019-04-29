---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 47cf87fce0af3b866018bf03a34a05ea42cef82c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426681"
---
# <a name="hrdoabdetailswithprovideruid"></a>HrDoABDetailsWithProviderUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt sicher, **** dass die OpenEntry-Methode vom erwarteten Exchange-Adressbuchanbieter geöffnet wird. Diese Funktion funktioniert ähnlich wie [IAddrBook::D ails](iaddrbook-details.md) , aber die **Eingabe** -Nr. wird mithilfe des von _pEmsabpUID_identifizierten Exchange-Adressbuchs geöffnet.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithProviderUID(
  const MAPIUID   *pEmsabpUID,
  LPADRBOOK        pAddrBook,
  ULONG_PTR FAR *  lpulUIParam,
  LPFNDISMISS      lpfnDismiss,
  LPVOID           lpvDismissContext,
  ULONG            cbEntryID,
  LPENTRYID        lpEntryID,
  LPFNBUTTON       lpfButtonCallback,
  LPVOID           lpvButtonContext,
  LPSTR           lpszButtonText,
  ULONG            ulFlags
);
```

## <a name="parameters"></a>Parameter

 _pEmsabpUID_
  
> in Ein Zeiger auf ein _emsabpUID_ , das den Exchange-Adressbuchanbieter identifiziert, der von dieser Funktion verwendet werden soll, um Details zur Eintrags-ID anzuzeigen. Wenn die ID des eingehenden Eintrags kein Exchange-Adressbuchanbieter ist, wird dieser Parameter ignoriert, und der Funktionsaufruf wirkt genau wie [IAddrBook::D ails](iaddrbook-details.md). Wenn dieser Parameter NULL oder eine NULL-MAPIUID ist, wirkt sich diese Funktion auch genau wie [IAddrBook::D ails](iaddrbook-details.md).
    
 _pAddrBook_
  
> in Das zum Öffnen des Eintrags Bezeichners verwendete Adressbuch. Er darf nicht NULL sein.
    
 _lpulUIParam_
  
> Out Ein Handle für das übergeordnete Fenster für das Dialogfeld.
    
 _lpfnDismiss_
  
> in Ein Zeiger auf eine Funktion, die auf dem **DISMISSMODELESS** -Prototyp basiert, oder NULL. Dieses Element gilt nur für die nicht modale Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI-Flag angegeben. MAPI Ruft die **DISMISSMODELESS** -Funktion auf, wenn der Benutzer das Dialogfeld nicht modale Adresse zurückweist und einen Client darüber informiert, dass das Dialogfeld nicht mehr aktiv ist. 
    
 _lpvDismissContext_
  
> in Ein Zeiger auf Kontextinformationen, die an die **DISMISSMODELESS** -Funktion übergeben werden, auf die durch den _lpfnDismiss_ -Parameter verwiesen wird. Dieser Parameter gilt nur für die nicht modale Version des Dialogfelds, indem das **DIALOG_SDI** -Flag im _ulFlags_ -Parameter eingeschlossen wird. 
    
 _cbEntryID_
  
> in Die Bytezahl der vom _lpEntryID_ -Parameter angegebenen Eintrags-ID. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID, die den zu öffnenden Adressbucheintrag darstellt.
    
 _lpfButtonCallback_
  
> in Ein Zeiger auf eine Funktion, die auf dem Prototyp der **LPFNBUTTON** -Funktion basiert. Mit einer **LPFNBUTTON** -Funktion wird dem Dialogfeld Details eine Schaltfläche hinzugefügt. 
    
 _lpvButtonContext_
  
> in Ein Zeiger auf Daten, die als Parameter für die durch den _lpfButtonCallback_ -Parameter angegebene Funktion verwendet wurden. 
    
 _lpszButtonText_
  
> in Ein Zeiger auf eine Zeichenfolge, die den Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist. Der Parameter _lpszButtonText_ sollte NULL sein, wenn eine erweiterbare Schaltfläche nicht erforderlich ist. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Texttyp für den _lpszButtonText_ -Parameter steuert. Die folgenden Flags können festgelegt werden: 
    
AB_TELL_DETAILS_CHANGE
  
> Gibt an, dass Details TRUE zurückgegeben werden, wenn tatsächlich Änderungen an der Adresse vorgenommen werden. Andernfalls gibt Details FALSE zurück.
    
DIALOG_MODAL
  
> Zeigt die modale Version des Dialogfelds allgemeine Adresse an. Dieses Flag ist mit DIALOG_SDI gegenseitig ausschließen.
    
DIALOG_SDI
  
> Zeigt die nicht modale Version des Dialogfelds allgemeine Adresse an. Dieses Flag ist mit DIALOG_MODAL gegenseitig ausschließen.
    
MAPI_UNICODE
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    

