---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3037187383cd5a00c96ce51c66950ee795e15052
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604831"
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
  
> [in] Ein Zeiger auf eine Nachrichtenklasse, die einem Empfangsordner zugeordnet ist. Wenn der  _Parameter lpszMessageClass_ auf NULL oder eine leere Zeichenfolge festgelegt ist, gibt **GetReceiveFolder** den Standard-Empfangsordner für den Nachrichtenspeicher zurück. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der übergebenen und zurückgegebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolge der Nachrichtenklasse hat das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, hat die Nachrichtenklassenzeichenfolge das ANSI-Format.
    
 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Byteanzahl im Eintragsbezeichner, auf den der  _Parameter "lppEntryID"_ verweist. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf den Eintragsbezeichner für den angeforderten Empfangsordner.
    
 _lppszExplicitClass_
  
> [out] Ein Zeiger auf einen Zeiger auf die Nachrichtenklasse, die den Ordner, auf den durch  _lppEntryID_ verwiesen wird, explizit als Empfangsordner festlegt. Diese Nachrichtenklasse sollte entweder mit der Klasse im  _LpszMessageClass-Parameter_ oder einer Basisklasse dieser Klasse identisch sein. Das Übergeben von NULL gibt an, dass der Ordner, auf den  _durch lppEntryID_ verwiesen wird, der Standard-Empfangsordner für den Nachrichtenspeicher ist. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Empfangsordner wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgStore::GetReceiveFolder-Methode** ruft den Eintragsbezeichner eines Empfangsordners ab, eines Ordners, der für den Empfang eingehender Nachrichten einer bestimmten Nachrichtenklasse vorgesehen ist. Aufrufer können eine Nachrichtenklasse oder NULL im  _LpszMessageClass-Parameter_ angeben. Wenn  _lpszMessageClass_ NULL ist, gibt **GetReceiveFolder** die folgenden Werte zurück: 
  
- In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder. 
    
- In  _lppEntryID_ der Eintragsbezeichner des Empfangsordners für die Basisklasse, auf die der  _Parameter lppszExplicitClass_ verweist. 
    
Angenommen, der Empfangsordner der Nachrichtenklasse **IPM. Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of _lpszMessageClass_ set to **IPM. Hinweis. Telefon**. Wenn **IPM. Hinweis. Telefon** hat keinen expliziten Empfangsordner festgelegt, **GetReceiveFolder** gibt den Eintragsbezeichner des Posteingangs in _lppEntryID_ und **IPM zurück. Hinweis** in _lppszExplicitClass_.
  
Wenn der Client **GetReceiveFolder** für eine Nachrichtenklasse aufruft und keinen Empfangsordner für diese Nachrichtenklasse festgelegt hat, ist  _lppszExplicitClass_ entweder eine Zeichenfolge der Länge Null, eine Zeichenfolge im Unicode-Format oder eine Zeichenfolge im ANSI-Format, je nachdem, ob der Client das flag MAPI_UNICODE im  _ulFlags-Parameter_ festgelegt hat. 
  
Ein standardmäßiger Empfangsordner, der durch Übergeben von NULL im  _LpszMessageClass-Parameter_ abgerufen wird, ist immer für jeden Nachrichtenspeicher vorhanden. 
  
Ein Client sollte die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen, wenn dies mit dem in  _lppEntryID zurückgegebenen_ Eintragsbezeichner erfolgt, um den Speicher freizugeben, der diesen Eintragsbezeichner enthält. Sie sollte auch **MAPIFreeBuffer** aufrufen, wenn sie mit der nachrichtenklassenzeichenfolge erfolgt, die in  _lppszExplicitClass_ zurückgegeben wird, um den Speicher freizugeben, der diese Zeichenfolge enthält. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |MFCMAPI verwendet die **IMsgStore::GetReceiveFolder-Methode,** um den Posteingangsordner zu suchen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

