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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f58bd8499b63bcd526906f78143b76092f194cb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792619"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

  
  
**Betrifft**: Outlook 
  
Ruft den Ordner, der als Ziel für eingehende Nachrichten von einer angegebenen Nachrichtenklasse oder als Standard Empfangsordner für den Nachrichtenspeicher eingerichtet wurde.
  
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
  
> [in] Ein Zeiger auf eine Nachrichtenklasse, die ein Empfangsordner zugeordnet ist. Wenn der Parameter _LpszMessageClass_ gibt NULL oder eine leere Zeichenfolge, **GetReceiveFolder** festgelegt ist die Standardeinstellung Ordner für den Nachrichtenspeicher empfangen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ der übergebenen und zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Klasse Meldungszeichenfolge ist im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, wird die Zeichenfolge der Klasse im ANSI-Format.
    
 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppEntryID_ verwiesen. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID für die angeforderte Empfangsordner.
    
 _lppszExplicitClass_
  
> [out] Ein Zeiger auf einen Zeiger auf die Nachrichtenklasse, die explizit als festlegt seine Empfangsordner im Ordner, die auf die _LppEntryID_zeigt. Diese Nachrichtenklasse sollte entweder der Klasse in der _LpszMessageClass_ -Parameter oder dieser Klasse eine Basisklasse identisch sein. Übergeben von NULL gibt an, dass der Ordner, auf die _LppEntryID_ zeigt den standardmäßigen Ordner für den Nachrichtenspeicher empfangen. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Empfangsordner wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::GetReceiveFolder** -Methode ruft die Eintrags-ID eines Ordners empfangen, einen Ordner, der zum Empfangen eingehender Nachrichten von einer bestimmten Nachrichtenklasse festgelegt. Anrufer können eine Nachrichtenklasse oder NULL in der _LpszMessageClass_ -Parameter angeben. Wenn _LpszMessageClass_ NULL ist, gibt **GetReceiveFolder** die folgenden Werte zurück: 
  
- In _LppszExplicitClass_auf die der Name des ersten-Basisklasse der Nachrichtenklasse _LpszMessageClass_ , die explizit eine Empfangsordner festgelegt wird. 
    
- In _LppEntryID_auf das die Eintrags-ID des Ordners empfangen der Basisklasse durch den Parameter _LppszExplicitClass_ . 
    
Nehmen wir beispielsweise bei den Empfangsordner der Nachrichtenklasse IPM **. Hinweis** festgelegt wurde dem Eintrag Bezeichner der Posteingang und **GetReceiveFolder** aufgerufen, mit dem Inhalt des _LpszMessageClass_ auf **IPM festgelegt. Note.Phone**. Wenn **IPM. Note.Phone** haben eine explizite erhält keine Ordner Set, **GetReceiveFolder** gibt die Eintrags-ID des Posteingangs in _LppEntryID_ und **IPM. Hinweis** in _LppszExplicitClass_.
  
Wenn der Client **GetReceiveFolder** für eine Nachrichtenklasse ruft und eine Empfangsordner für die Nachrichtenklasse nicht festgelegt wurde, _LppszExplicitClass_ ist entweder eine leere Zeichenfolge, eine Zeichenfolge im Unicode-Format oder eine Zeichenfolge im ANSI-Format, je nachdem, ob die Client legen Sie die Option MAPI_UNICODE im _UlFlags_ -Parameter. 
  
Ein standardmäßiges Empfangsordner abgerufen, indem Sie NULL im _LpszMessageClass_ -Parameter übergeben, ist für jedes Nachrichtenspeicher immer vorhanden. 
  
Ein Client sollte die Funktion [MAPIFreeBuffer](mapifreebuffer.md) aufrufen, wenn er, mit der Eintrags-ID, die in _LppEntryID abgeschlossen ist_ , um den Arbeitsspeicher freizugeben, der die Eintrags-ID zurückgegeben. Sie sollten auch **MAPIFreeBuffer** aufrufen, wenn er, mit der Klassenzeichenfolge zurückgegeben, die in _LppszExplicitClass abgeschlossen ist_ , um den Arbeitsspeicher freizugeben, der die Zeichenfolge enthält. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |MFCMAPI (engl.) verwendet die **IMsgStore::GetReceiveFolder** -Methode, um den Ordner Posteingang zu suchen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

