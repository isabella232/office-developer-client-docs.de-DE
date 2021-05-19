---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421368"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt sicher, **dass die OpenEntry-Methode** vom erwarteten Adressbuchanbieter Exchange geöffnet wird. Diese Funktion funktioniert ähnlich wie [IAddrBook::D etails](iaddrbook-details.md), öffnet jedoch die **entryID** mit dem Exchange, das durch den _pEmsmdbUID-Parameter_ identifiziert wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
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
  
> Die angemeldete **IMAPISession**. Es kann nicht NULL sein.
    
 _pEmsmdbUID_
  
> Ein Zeiger auf eine **emsmdbUID,** die den Exchange-Dienst identifiziert, der den Exchange-Adressbuchanbieter enthält, der von der Funktion zum Öffnen der Eintrags-ID verwendet wird. Wenn der Bezeichner für eingehende Exchange keine Adressbuchanbietereintrags-ID ist, wird dieser Parameter ignoriert, und die Funktion verhält sich wie [IAddrBook::OpenEntry](iaddrbook-openentry.md). Wenn dieser Parameter NULL oder null **MAPIUID** ist, funktioniert diese Funktion genauso wie [IAddrBook::OpenEntry](iaddrbook-openentry.md). 
    
 _pAddrBook_
  
> [in] Das Adressbuch, das zum Öffnen der Eintrags-ID verwendet wird. Es kann nicht NULL sein.
    
 _lpulUIParam_
  
> [out] Ein Handle zum übergeordneten Fenster für das Dialogfeld.
    
 _lpfnDismiss_
  
> [in] Ein Zeiger auf eine Funktion basierend auf dem **DISMISSMODELESS-Prototyp** oder NULL. Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI angegeben wird. MAPI ruft die **FUNKTION DISMISSMODELESS** auf, wenn der Benutzer das Dialogfeld "Modeless Address" schließt und einen Client informiert, der Details aufruft, dass das Dialogfeld nicht mehr aktiv ist. 
    
 _lpvDismissContext_
  
> [in] Ein Zeiger auf Kontextinformationen, der an die **DISMISSMODELESS-Funktion übergeben** wird, auf die der  _lpfnDismiss-Parameter_ verweist. Dieser Parameter gilt nur für die moduslose Version  des Dialogfelds, indem das DIALOG_SDI im _ulFlags-Parameter verwendet_ wird. 
    
 _cbEntryID_
  
> [in] Die Byteanzahl des Eintragsbezeichners, der durch den  _lpEntryID-Parameter angegeben_ wird. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnende Adressbucheintrag darstellt.
    
 _lpfButtonCallback_
  
> [in] Ein Zeiger auf eine Funktion basierend auf dem **LPFNBUTTON-Funktionsprototyp.** Eine **LPFNBUTTON-Funktion** fügt dem Dialogfeld Details eine Schaltfläche hinzu. 
    
 _lpvButtonContext_
  
> [in] Ein Zeiger auf Daten, die als Parameter für die durch den  _lpfButtonCallback-Parameter_ angegebene Funktion verwendet wurden. 
    
 _lpszButtonText_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist. Der  _lpszButtonText-Parameter_ sollte NULL sein, wenn keine erweiterbare Schaltfläche erforderlich ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Texttyp für den  _lpszButtonText-Parameter_ steuert. Die folgenden Kennzeichen können festgelegt werden: 
    
AB_TELL_DETAILS_CHANGE
  
> Gibt an, dass Details TRUE zurückgibt, wenn tatsächlich Änderungen an der Adresse vorgenommen werden. Andernfalls gibt Details FALSE zurück.
    
DIALOG_MODAL
  
> Zeigt die modale Version des Dialogfelds allgemeine Adresse an. Dieses Flag schließen sich gegenseitig mit DIALOG_SDI.
    
DIALOG_SDI
  
> Zeigt die moduslose Version des Dialogfelds allgemeine Adresse an. Dieses Flag schließen sich gegenseitig mit DIALOG_MODAL.
    
MAPI_UNICODE
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    

