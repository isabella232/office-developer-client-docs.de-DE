---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c30c38e1dbc944fd3016badf2621aef5de1e08f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792650"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**Betrifft**: Outlook 
  
Stellt einen Ordner als Ziel für eingehende Nachrichten von einer bestimmten Nachrichtenklasse her.
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameter

 _lpszMessageClass_
  
> [in] Empfangsordner für ein Zeiger auf die Nachrichtenklasse, die mit dem neuen zugeordnet werden soll. Wenn der _LpszMessageClass_ -Parameter auf NULL oder eine leere Zeichenfolge, **SetReceiveFolder** festgelegt werden standardmäßig Ordner für den Nachrichtenspeicher empfangen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ des Texts in den übergebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Klasse Meldungszeichenfolge ist im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, wird die Zeichenfolge der Klasse im ANSI-Format.
    
 _cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Ordners, der als den Empfangsordner einzurichten. Der _LpEntryID_ -Parameter auf NULL **SetReceiveFolder** ersetzt festgelegt ist empfangen die aktuelle Ordner mit der Nachrichtenspeicher Standard. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Eine Empfangsordner wurde erfolgreich hergestellt.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::SetReceiveFolder** -Methode legt oder ändert den Empfangsordner für eine bestimmte Nachrichtenklasse. Mit **SetReceiveFolder**kann einen Client mithilfe von aufeinander folgenden Aufrufen angeben, ein anderes Empfangsordner für jede definierte Nachrichtenklasse oder angeben, dass eingehende Nachrichten für mehrere Nachrichtenklassen alle im gleichen Ordner wechseln. Ein Client kann beispielsweise eine eigene Klasse von Nachrichten in einem eigenen Ordner eintreffen haben. Eine Anwendung Fax kann festlegen, einen Ordner, in dem Speicheranbieter eingehende Faxe versetzt, und einen anderen Ordner, in dem der Anbieter Ausgehende Faxnachrichten versetzt.
  
Wenn ein Fehler während des Aufrufs von **SetReceiveFolder**auftritt, bleibt die Einstellung für den empfangen unverändert. 
  
Wenn **SetReceiveFolder** ändert festgelegt die Einstellung für den Empfang mit _LpEntryID_ auf NULL wurde, was bedeutet, dass im Standardordner empfangen festgelegt werden sollte, **SetReceiveFolder** gibt S_OK zurück, auch wenn es wurde keine Einstellung für die angegebene Message-Klasse. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnSetReceiveFolder  <br/> |MFCMAPI (engl.) verwendet die **IMsgStore::SetReceiveFolder** -Methode, um einen Ordner als den Empfangsordner für eine bestimmte Nachrichtenklasse festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

