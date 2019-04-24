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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5fbd20a6b5d5598b8fa51f9c369eefac9a1ea2e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341720"
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
  
> in Ein Zeiger auf ein Handle des übergeordneten Fensters für das Dialogfeld.
    
 _lpfnDismiss_
  
> in Ein Zeiger auf eine Funktion, die auf dem [DISMISSMODELESS](dismissmodeless.md) -Prototyp basiert, oder NULL. Dieses Element gilt nur für die nicht modale Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI-Flag angegeben. MAPI Ruft die **DISMISSMODELESS** -Funktion auf, wenn der Benutzer das Dialogfeld nicht modale Adresse zurückweist und einen Client darüber informiert, **** dass das Dialogfeld nicht mehr aktiv ist. 
    
 _lpvDismissContext_
  
> in Ein Zeiger auf Kontextinformationen, die an die **DISMISSMODELESS** -Funktion übergeben werden, auf die durch den _lpfnDismiss_ -Parameter verwiesen wird. Dieser Parameter gilt nur für die nicht modale Version des Dialogfelds, indem das DIALOG_SDI-Flag im _ulFlags_ -Parameter eingeschlossen wird. 
    
 _cbEntryID_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID für den Eintrag, für den Details angezeigt werden.
    
 _lpfButtonCallback_
  
> in Ein Zeiger auf eine Funktion, die auf dem Prototyp der [LPFNBUTTON](lpfnbutton.md) -Funktion basiert. Mit einer **LPFNBUTTON** -Funktion wird dem Dialogfeld Details eine Schaltfläche hinzugefügt. 
    
 _lpvButtonContext_
  
> in Ein Zeiger auf Daten, die als Parameter für die durch den _lpfButtonCallback_ -Parameter angegebene Funktion verwendet wurden. 
    
 _lpszButtonText_
  
> in Ein Zeiger auf eine Zeichenfolge, die den Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist. Der _lpszButtonText_ -Parameter sollte NULL sein, wenn Sie keine erweiterbare Schaltfläche benötigen. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Texttyp für den _lpszButtonText_ -Parameter steuert. Die folgenden Flags können festgelegt werden: 
    
AB_TELL_DETAILS_CHANGE
  
> Gibt an, dass **Details** S_OK zurückgegeben werden, wenn tatsächlich Änderungen an der Adresse vorgenommen werden. Andernfalls gibt **Details** S_FALSE zurück. 
    
DIALOG_MODAL
  
> Zeigt die modale Version des Dialogfelds allgemeine Adresse an, das immer in nicht-Outlook-Clients angezeigt wird. Dieses Flag ist mit DIALOG_SDI gegenseitig ausschließen.
    
DIALOG_SDI
  
>  Zeigt die nicht modale Version des Dialogfelds allgemeine Adresse an. Dieses Flag wird für nicht-Outlook-Clients ignoriert. 
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Dialogfeld Details wurde erfolgreich für den Adressbucheintrag angezeigt.
    
## <a name="remarks"></a>Bemerkungen

Client Anwendungen rufen die **Details** -Methode auf, um ein Dialogfeld anzuzeigen, das Details zu einem bestimmten Eintrag im Adressbuch bereitstellt. Sie können die Parameter _lpfButtonCallback_, _lpvButtonContext_und _lpszButtonText_ verwenden, um dem Dialogfeld eine Client definierte Schaltfläche hinzuzufügen. Wenn auf die Schaltfläche geklickt wird, ruft MAPI die Rückruffunktion auf, auf die von _lpfButtonCallback_verwiesen wird, wobei sowohl die Eintrags-ID der Schaltfläche als auch die Daten in _lpvButtonContext_übergeben werden. Wenn Sie keine erweiterbare Schaltfläche benötigen, sollte _LPSZBUTTONTEXT_ NULL sein. 
  
 **Details** unterstützt Unicode-Zeichenfolgen; Unicode-Zeichenfolgen werden in das Multibyte Character String-Format (MBCS) konvertiert, bevor Sie im Dialogfeld Details angezeigt werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog:: OnOpenEntryID  <br/> |MFCMAPI verwendet die **Details** -Methode, um ein Dialogfeld anzuzeigen, in dem die Details für einen Adressbucheintrag angezeigt werden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

