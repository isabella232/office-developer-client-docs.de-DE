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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1cfd4afbda5892e96a1d74ca56f4a6d1f98e2268
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792343"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**Betrifft**: Outlook 
  
Erstellt einen Eintrag Bezeichner für eine einmalige Adresse.
  
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

 _Wert_
  
> [in] Ein Zeiger auf den Anzeigenamen des Empfängers die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft. Der _Wert_ -Parameter kann NULL sein. 
    
 _lpszAdrType_
  
> [in] Ein Zeiger auf den Adresstyp (wie FAX, SMTP oder X500) des Empfängers. Der Parameter _LpszAdrType_ darf nicht NULL sein. 
    
 _lpszAddress_
  
> [in] Ein Zeiger auf die messaging-Adresse des Empfängers. Der Parameter _LpszAddress_ darf nicht NULL sein. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den einmal-Empfänger auswirkt. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_SEND_NO_RICH_INFO 
  
> Der Empfänger kann nicht formatierte Nachrichteninhalt behandeln. Wenn MAPI_SEND_NO_RICH_INFO festgelegt ist, wird der MAPI-Eigenschaft des Empfängers- **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) auf false festgelegt. Wenn MAPI_SEND_NO_RICH_INFO nicht festgelegt ist, wird diese Eigenschaft von MAPI auf TRUE festgelegt, es sei denn, die Adresse des Empfängers messaging auf das _LpszAddress_ interpretiert wird, um eine IP-Adresse sein. In diesem Fall wird MAPI **PR_SEND_RICH_INFO** auf false festgelegt. 
    
PARAMETER MAPI_UNICODE 
  
> Der Anzeigename, Adresstyp und Adresse sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen in ANSI-Format.
    
 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Anzahl von Bytes in die Eintrags-ID auf den durch den Parameter _LppEntryID_ verwiesen. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den einmaligen Empfänger.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Bezeichner des Eingangs wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::CreateOneOff** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert. Dienstanbieter anrufen **CreateOneOff** zum Erstellen eines Eintrags-ID für einen einmaligen Empfänger (Empfänger, die nicht zu keiner der Container aus der aktuell geladenen adressbuchanbietern implementierte gehört). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie die Eintrags-ID von **CreateOneOff**zurückgegeben werden, frei Arbeitsspeichers für die Eintrags-ID mithilfe der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion. 
  
## <a name="notes-to-transport-providers"></a>Hinweise für Transport-Anbieter

Unterstützen Sie der Transport Neutral Encapsulation Format (TNEF), und verwenden Sie den Wert der Eigenschaft **PR_SEND_RICH_INFO** um zu ermitteln, ob TNEF verwenden, wenn Sie eine Nachricht transport. TNEF nicht unterstützt, oder Senden einer Nachricht nicht in diesem Format aus, wenn sie dazu aufgefordert werden möglicherweise ein Problem für formularbasierte oder Clients, die eine benutzerdefinierte MAPI-Eigenschaften erfordern. Dies ist, da TNEF in der Regel zum Senden von benutzerdefinierter Eigenschaften für benutzerdefinierte Nachrichtenklassen verwendet wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Kanonische PidTagDisplayName-Eigenschaft](pidtagdisplayname-canonical-property.md)
  
[Kanonische PidTagSendRichInfo-Eigenschaft](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

