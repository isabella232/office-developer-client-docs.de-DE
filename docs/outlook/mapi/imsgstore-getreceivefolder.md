---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ab21dcfb9011b675e3db4e4df29cb6ecafa6e7c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435348"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft den Ordner ab, der als Ziel für eingehende Nachrichten einer angegebenen Nachrichtenklasse oder als Standard-Empfangsordner für den Nachrichtenspeicher eingerichtet wurde.
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a>Parameter

 _lpszMessageClass_
  
> [in] Ein Zeiger auf eine Nachrichtenklasse, die einem Empfangsordner zugeordnet ist. Wenn der  _lpszMessageClass-Parameter_ auf NULL oder eine leere Zeichenfolge festgelegt ist, gibt **GetReceiveFolder** den Standard-Empfangsordner für den Nachrichtenspeicher zurück. 
    
 _ulFlags_
  
> [in] Eine Bitmaske von Flags, die den Typ der übergebenen und zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolge der Nachrichtenklasse befindet sich im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Zeichenfolge der Nachrichtenklasse im ANSI-Format.
    
 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Byteanzahl in der Eintrags-ID, auf die der  _lppEntryID-Parameter_ verweist. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den angeforderten Empfangsordner.
    
 _lppszExplicitClass_
  
> [out] Ein Zeiger auf einen Zeiger auf die Nachrichtenklasse, die explizit als Empfangsordner festgelegt wird, auf den der Ordner durch _lppEntryID verweist._ Diese Nachrichtenklasse sollte entweder mit der Klasse im  _lpszMessageClass-Parameter_ oder einer Basisklasse dieser Klasse identisch sein. Das Übergeben von NULL gibt an, dass der Ordner, auf den  _lppEntryID_ verweist, der Standard-Empfangsordner für den Nachrichtenspeicher ist. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Empfangsordner wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::GetReceiveFolder-Methode** ruft die Eintrags-ID eines Empfangsordners ab, einem Ordner, der für den Empfang eingehender Nachrichten einer bestimmten Nachrichtenklasse bestimmt ist. Anrufer können eine Nachrichtenklasse oder NULL im  _lpszMessageClass-Parameter_ angeben. Wenn  _lpszMessageClass_ null ist, **gibt GetReceiveFolder** die folgenden Werte zurück: 
  
- In  _lppszExplicitClass_ der Name der ersten Basisklasse der Nachrichtenklasse, auf die  _von lpszMessageClass_ verwiesen wird, die explizit einen Empfangsordner festgelegt hat. 
    
- In  _lppEntryID_ der Eintragsbezeichner des Empfangsordners für die Basisklasse, auf die der  _lppszExplicitClass-Parameter_ verweist. 
    
Angenommen, der Empfangsordner der Nachrichtenklasse **IPM. Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of _lpszMessageClass_ set to **IPM. Hinweis. Telefon**. Wenn **IPM. Hinweis. Telefon** hat keinen expliziten Empfangsordnersatz, **gibt GetReceiveFolder** den Eintragsbezeichner des Posteingangs in _lppEntryID_ und **IPM zurück. Hinweis** in _lppszExplicitClass_.
  
Wenn der Client **GetReceiveFolder** für eine Nachrichtenklasse aufruft und keinen Empfangsordner für diese Nachrichtenklasse festgelegt hat, ist  _lppszExplicitClass_ entweder eine Nulllängenzeichenfolge, eine Zeichenfolge im Unicode-Format oder eine Zeichenfolge im ANSI-Format, je nachdem, ob der Client das MAPI_UNICODE-Flag im  _ulFlags-Parameter_ festgelegt hat. 
  
Ein Standardmäßiger Empfangsordner, der durch Übergeben von NULL im  _lpszMessageClass-Parameter_ erhalten wird, ist immer für jeden Nachrichtenspeicher vorhanden. 
  
Ein Client sollte die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen, wenn dies mit dem in  _lppEntryID zurückgegebenen_ Eintragsbezeichner erfolgt, um den Speicher frei zu machen, der diese Eintrags-ID enthält. Es sollte auch **MAPIFreeBuffer** aufrufen, wenn dies mit der in  _lppszExplicitClass_ zurückgegebenen Nachrichtenklassenzeichenfolge erfolgt, um den Speicher frei zu machen, der diese Zeichenfolge enthält. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |MFCMAPI verwendet die **IMsgStore::GetReceiveFolder-Methode,** um den Posteingangsordner zu finden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

