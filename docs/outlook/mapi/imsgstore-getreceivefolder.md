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
  
Ruft den Ordner ab, der als Ziel für eingehende Nachrichten einer angegebenen Nachrichtenklasse oder als standardmäßiger Empfangsordner für den Nachrichtenspeicher eingerichtet wurde.
  
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
  
> in Ein Zeiger auf eine Nachrichtenklasse, die einem Empfangsordner zugeordnet ist. Wenn der Parameter _lpszMessageClass_ auf NULL oder eine leere Zeichenfolge festgelegt ist, gibt **GetReceiveFolder** den standardmäßigen Empfangsordner für den Nachrichtenspeicher zurück. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der übergebenen und zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolge der Nachrichtenklasse ist im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Zeichenfolge der Nachrichtenklasse im ANSI-Format.
    
 _lpcbEntryID_
  
> Out Ein Zeiger auf die Bytezahl in der Eintrags-ID, auf die durch den _lppEntryID_ -Parameter verwiesen wird. 
    
 _lppEntryID_
  
> Out Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den angeforderten Empfänger Ordner.
    
 _lppszExplicitClass_
  
> Out Ein Zeiger auf einen Zeiger auf die Nachrichtenklasse, die explizit als der Empfänger Ordner den Ordner, auf den durch _lppEntryID_festgelegt wird. Diese Nachrichtenklasse sollte entweder mit der Klasse im _lpszMessageClass_ -Parameter oder mit einer Basisklasse dieser Klasse übereinstimmen. Die Übergabe von NULL gibt an, dass der Ordner, auf den von _lppEntryID_ verwiesen wird, der standardmäßige Empfangsordner für den Nachrichtenspeicher ist. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Empfangsordner wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore:: GetReceiveFolder** -Methode ruft die Eintrags-ID eines Empfangs Ordners ab, einen Ordner, der zum Empfangen eingehender Nachrichten einer bestimmten Nachrichtenklasse bestimmt ist. Anrufer können eine Nachrichtenklasse oder einen NULL-Wert im _lpszMessageClass_ -Parameter angeben. Wenn _lpszMessageClass_ ist, gibt **GetReceiveFolder** die folgenden Werte zurück: 
  
- In _lppszExplicitClass_der Name der ersten Basisklasse der Nachrichtenklasse, auf die durch _lpszMessageClass_ verwiesen wird, der explizit einen Empfangsordner festgelegt hat. 
    
- In _lppEntryID_wird die Eintrags-ID des Empfänger Ordners für die Basisklasse, auf die durch den _lppszExplicitClass_ -Parameter verwiesen wird. 
    
Angenommen, der Empfangsordner der Nachrichtenklasse **IPM. Hinweis** wurde auf die Eintrags-ID des Posteingangs festgelegt, und **GetReceiveFolder** wird aufgerufen, wenn der Inhalt von _lpszMessageClass_ auf IPM festgelegt ist **. Hinweis. Phone**. Wenn **IPM. Hinweis. das Telefon** verfügt nicht über einen expliziten Empfänger Ordner, **GetReceiveFolder** gibt den Eintragsbezeichner des Posteingangs in _lppEntryID_ und **IPM zurück. Hinweis** in _lppszExplicitClass_.
  
Wenn der Client **GetReceiveFolder** für eine Nachrichtenklasse aufruft und keinen Empfangsordner für diese Nachrichtenklasse festgelegt hat, ist _lppszExplicitClass_ entweder eine leere Zeichenfolge, eine Zeichenfolge im Unicode-Format oder eine Zeichenfolge im ANSI-Format, je nachdem, ob die Client legen Sie das MAPI_UNICODE-Flag im _ulFlags_ -Parameter fest. 
  
Ein standardmäßiger Empfangsordner, der durch Übergeben von NULL im _lpszMessageClass_ -Parameter abgerufen wird, ist immer für jeden Nachrichtenspeicher vorhanden. 
  
Ein Client sollte die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen, wenn er mit der in _lppEntryID_ zurückgegebenen Eintrags-ID ausgeführt wird, um den Speicher freizugeben, der diese Eintrags-ID enthält. Sie sollte auch **mapifreebufferfreigegeben** aufrufen, wenn Sie mit der in _lppszExplicitClass_ zurückgegebenen Nachrichtenklassen Zeichenfolge ausgeführt wird, um den Speicher freizugeben, der diese Zeichenfolge enthält. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetInbox  <br/> |MFCMAPI verwendet die **IMsgStore:: GetReceiveFolder** -Methode, um den Ordner Posteingang zu suchen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

