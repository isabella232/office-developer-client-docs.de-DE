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
ms.openlocfilehash: fbe7f02555f76532896c951f50648c528c250a58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792013"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
**Betrifft**: Outlook 
  
Zeigt ein Dialogfeld, das Details zu einem bestimmten Buch Adresseintrag anzeigt.
  
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
  
> [in] Ein Zeiger auf ein Handle für das übergeordnete Fenster für das Dialogfeld.
    
 _lpfnDismiss_
  
> [in] Ein Zeiger auf eine Funktion, die basierend auf dem [DISMISSMODELESS](dismissmodeless.md) Prototyp oder NULL. Dieser Member gilt nur für die im Dialogfeld ohne Modus Version durch das DIALOG_SDI-Flag festgelegt wird. MAPI-Aufrufen die **DISMISSMODELESS** -Funktion, wenn der Benutzer schließt das Dialogfeld ohne Modus Adresse informiert einen Client, der **Details** anruft, dass das Dialogfeld nicht mehr aktiv ist. 
    
 _lpvDismissContext_
  
> [in] Ein Zeiger auf Kontextinformationen zum Übergeben an die Funktion **DISMISSMODELESS** an, durch den Parameter _LpfnDismiss_ auf. Dieser Parameter gilt nur für die im Dialogfeld ohne Modus Version durch das DIALOG_SDI-Flag in den Parameter _UlFlags_ einschließen. 
    
 _cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID für den Eintrag für den Details angezeigt werden.
    
 _lpfButtonCallback_
  
> [in] Ein Zeiger auf eine Funktion, die basierend auf den [LPFNBUTTON](lpfnbutton.md) Funktionsprototyp. Eine **LPFNBUTTON** -Funktion hinzugefügt im Dialogfeld Details der eine Schaltfläche. 
    
 _lpvButtonContext_
  
> [in] Ein Zeiger auf Daten, die als Parameter für die Funktion, die durch den _LpfButtonCallback_ -Parameter angegebenen verwendet wurde. 
    
 _lpszButtonText_
  
> [in] Ein Zeiger auf eine Zeichenfolge mit Text auf die Schaltfläche hinzugefügt, angewendet werden soll, wenn diese Schaltfläche erweiterbar ist. Der Parameter _LpszButtonText_ sollte NULL sein, wenn Sie nicht über eine Schaltfläche extensible benötigen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ des Texts für den Parameter _LpszButtonText_ steuert. Die folgenden Kennzeichen können festgelegt werden: 
    
AB_TELL_DETAILS_CHANGE
  
> Gibt an, dass **Details** gibt S_OK zurück, wenn die Adresse; tatsächlich geändert werden **Details** haben andernfalls S_FALSE. 
    
DIALOG_MODAL
  
> Anzeigen der modalen Version allgemeine Adresse im Dialogfeld, der immer in nicht-Outlook-Clients angezeigt wird. Dieses Kennzeichen ist mit DIALOG_SDI gegenseitig aus.
    
DIALOG_SDI
  
>  Die ohne Modus Version von der Adresse Standarddialogfeld angezeigt. Dieses Kennzeichen werden für nicht-Outlook-Clients ignoriert. 
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Im Dialogfeld Details der wurde erfolgreich für den Adresseintrag Adressbuch angezeigt.
    
## <a name="remarks"></a>Hinweise

Clientanwendungen rufen Sie die **Details** -Methode, um ein Dialogfeld angezeigt, das Details zu einem bestimmten Eintrag im Adressbuch bereitstellt. Der Parameter _LpfButtonCallback_, _LpvButtonContext_und _LpszButtonText_ können, um das Dialogfeld eine Schaltfläche Client definiert hinzuzufügen. Wenn auf die Schaltfläche geklickt wird, ruft MAPI die Callback-Funktion, die auf den _LpfButtonCallback_, sowohl die Eintrags-ID für die Schaltfläche und die Daten in _LpvButtonContext_übergeben. Wenn Sie eine extensible Schaltfläche nicht erforderlich ist, sollte _LpszButtonText_ NULL sein. 
  
 **Details** unterstützt Unicode-Zeichenfolgen. Unicode-Zeichenfolgen werden in der multibyte-Zeichenfolge handeln Zeichenformat konvertiert, bevor sie im Dialogfeld Details angezeigt werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnOpenEntryID  <br/> |MFCMAPI (engl.) verwendet die **Details** -Methode, um ein Dialogfeld angezeigt, das Details für ein Buch Adresseintrag anzeigt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

