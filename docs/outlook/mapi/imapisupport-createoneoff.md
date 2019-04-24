---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9571d51e01c2d58d9b8a9a913ba2c210ae0bd44d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322401"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine Eintrags-ID für eine einmalige Adresse.
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameter

 _lpszName_
  
> in Ein Zeiger auf den Anzeigenamen des Empfängers die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft. Der _lpszName_ -Parameter kann NULL sein. 
    
 _lpszAdrType_
  
> in Ein Zeiger auf den Adresstyp (wie FAX, SMTP oder x500) des Empfängers. Der _lpszAdrType_ -Parameter darf nicht NULL sein. 
    
 _lpszAddress_
  
> in Ein Zeiger auf die Messaging Adresse des Empfängers. Der _lpszAddress_ -Parameter darf nicht NULL sein. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die sich auf den einmaligen Empfänger auswirkt. Die folgenden Flags können festgelegt werden:
    
MAPI_SEND_NO_RICH_INFO 
  
> Der Empfänger kann formatierten Nachrichteninhalt nicht verarbeiten. Wenn MAPI_SEND_NO_RICH_INFO festgelegt ist, legt MAPI die **PR_SEND_RICH_INFO** ([pidtagsendrichinfo (](pidtagsendrichinfo-canonical-property.md))-Eigenschaft des Empfängers auf false fest. Wenn MAPI_SEND_NO_RICH_INFO nicht festgelegt ist, legt MAPI diese Eigenschaft auf TRUE fest, es sei denn, die Messaging Adresse des Empfängers, auf die durch _lpszAddress_ verwiesen wird, wird als Internet Adresse interpretiert. In diesem Fall wird **PR_SEND_RICH_INFO** auf false festgelegt. 
    
MAPI_UNICODE 
  
> Der Anzeigename, der Adresstyp und die Adresse sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind diese Zeichenfolgen im ANSI-Format.
    
 _lpcbEntryID_
  
> Out Ein Zeiger auf die Anzahl von Bytes in der Eintrags-ID, auf die durch den _lppEntryID_ -Parameter verwiesen wird. 
    
 _lppEntryID_
  
> Out Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den einmaligen Empfänger.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der einmalige Eintragsbezeichner wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: CreateOneOff** -Methode wird für alle Support Objekte des Dienstanbieters implementiert. Dienstanbieter rufen **CreateOneOff** auf, um eine Eintrags-ID für einen einmaligen Empfänger (einen Empfänger, der keinem der Container von einem der derzeit geladenen Adressbuchanbieter gehört) zu erstellen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie die von **CreateOneOff**zurückgegebene Eintrags-ID nicht mehr verwenden möchten, müssen Sie den für die Eintrags-ID reservierten Arbeitsspeicher mithilfe der [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion freigeben. 
  
## <a name="notes-to-transport-providers"></a>Hinweise für Transport Anbieter

Unterstützen Sie das Transport Neutral Encapsulation Format (TNEF), und verwenden Sie den Wert der **PR_SEND_RICH_INFO** -Eigenschaft, um zu bestimmen, ob TNEF beim Transport einer Nachricht verwendet werden soll. Wenn Sie TNEF nicht unterstützen oder keine Nachricht in diesem Format senden, wenn Sie angefordert wird, kann dies ein Problem für formularbasierte Clients oder Clients sein, die benutzerdefinierte MAPI-Eigenschaften erfordern. Der Grund ist, dass TNEF in der Regel zum Senden benutzerdefinierter Eigenschaften für benutzerdefinierte Nachrichtenklassen verwendet wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Kanonische PidTagDisplayName-Eigenschaft](pidtagdisplayname-canonical-property.md)
  
[Kanonische Pidtagsendrichinfo (-Eigenschaft](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

