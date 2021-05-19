---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5fbd20a6b5d5598b8fa51f9c369eefac9a1ea2e9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424679"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt ein Dialogfeld an, in dem Details zu einem bestimmten Adressbucheintrag angezeigt werden.
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulUIParam_
  
> [in] Ein Zeiger auf ein Handle des übergeordneten Fensters für das Dialogfeld.
    
 _lpfnDismiss_
  
> [in] Ein Zeiger auf eine Funktion basierend auf dem [DISMISSMODELESS-Prototyp](dismissmodeless.md) oder NULL. Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI angegeben wird. MAPI ruft die **FUNKTION DISMISSMODELESS** auf, wenn der Benutzer das Dialogfeld "Modeless Address" schließt und einen Client informiert, der **Details** aufruft, dass das Dialogfeld nicht mehr aktiv ist. 
    
 _lpvDismissContext_
  
> [in] Ein Zeiger auf Kontextinformationen, der an die **DISMISSMODELESS-Funktion übergeben** wird, auf die der  _lpfnDismiss-Parameter_ verweist. Dieser Parameter gilt nur für die moduslose Version des Dialogfelds, indem das DIALOG_SDI im  _ulFlags-Parameter verwendet_ wird. 
    
 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID für den Eintrag, für den Details angezeigt werden.
    
 _lpfButtonCallback_
  
> [in] Ein Zeiger auf eine Funktion basierend auf dem [LPFNBUTTON-Funktionsprototyp.](lpfnbutton.md) Eine **LPFNBUTTON-Funktion** fügt dem Dialogfeld Details eine Schaltfläche hinzu. 
    
 _lpvButtonContext_
  
> [in] Ein Zeiger auf Daten, die als Parameter für die durch den  _lpfButtonCallback-Parameter_ angegebene Funktion verwendet wurden. 
    
 _lpszButtonText_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist. Der  _lpszButtonText-Parameter_ sollte NULL sein, wenn Sie keine erweiterbare Schaltfläche benötigen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Texttyp für den  _lpszButtonText-Parameter_ steuert. Die folgenden Kennzeichen können festgelegt werden: 
    
AB_TELL_DETAILS_CHANGE
  
> Gibt an, dass **Details** S_OK, wenn tatsächlich Änderungen an der Adresse vorgenommen werden. Andernfalls **gibt Details** S_FALSE. 
    
DIALOG_MODAL
  
> Zeigen Sie die modale Version des Dialogfelds allgemeine Adresse an, das immer in Nicht-Outlook angezeigt wird. Dieses Flag schließen sich gegenseitig mit DIALOG_SDI.
    
DIALOG_SDI
  
>  Zeigt die moduslose Version des Dialogfelds allgemeine Adresse an. Dieses Flag wird für Nicht-Outlook ignoriert. 
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Dialogfeld Details wurde erfolgreich für den Adressbucheintrag angezeigt.
    
## <a name="remarks"></a>Hinweise

Clientanwendungen rufen die **Details-Methode** auf, um ein Dialogfeld anzuzeigen, das Details zu einem bestimmten Eintrag im Adressbuch enthält. Sie können die Parameter  _lpfButtonCallback,_  _lpvButtonContext_ und  _lpszButtonText_ verwenden, um dem Dialogfeld eine clientdefinierte Schaltfläche hinzuzufügen. Wenn auf die Schaltfläche geklickt wird, ruft MAPI die Rückruffunktion auf, auf die von _lpfButtonCallback_ verwiesen wird. Dabei wird sowohl der Eintragsbezeichner der Schaltfläche als auch die Daten in _lpvButtonContext übergeben._ Wenn Sie keine erweiterbare Schaltfläche benötigen,  _sollte lpszButtonText_ NULL sein. 
  
 **Details** unterstützen Unicode-Zeichenzeichenfolgen; Unicode-Zeichenfolgen werden in das MbCS-Format (MultiByte Character String) konvertiert, bevor sie im Dialogfeld Details angezeigt werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnOpenEntryID  <br/> |MFCMAPI verwendet die **Details-Methode,** um ein Dialogfeld anzuzeigen, in dem die Details für einen Adressbucheintrag angezeigt werden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

