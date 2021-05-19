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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: efa5d60098fd5f16328669249a8445a124d9878b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434088"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Richtet einen Ordner als Ziel für eingehende Nachrichten einer bestimmten Nachrichtenklasse ein.
  
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
  
> [in] Ein Zeiger auf die Nachrichtenklasse, die dem neuen Empfangsordner zugeordnet werden soll. Wenn der  _lpszMessageClass-Parameter_ auf NULL oder eine leere Zeichenfolge festgelegt ist, legt **SetReceiveFolder** den Standard-Empfangsordner für den Nachrichtenspeicher fest. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Texttyp in den übergebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolge der Nachrichtenklasse befindet sich im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Zeichenfolge der Nachrichtenklasse im ANSI-Format.
    
 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Ordners, der als Empfangsordner erstellt werden soll. Wenn der  _lpEntryID-Parameter_ auf NULL festgelegt ist, ersetzt **SetReceiveFolder** den aktuellen Empfangsordner durch den Standard des Nachrichtenspeichers. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Ein Empfangsordner wurde erfolgreich eingerichtet.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::SetReceiveFolder-Methode** legt den Empfangsordner für eine bestimmte Nachrichtenklasse fest oder ändert diesen. Mit **SetReceiveFolder** kann ein Client mithilfe aufeinander folgenden Aufrufe einen anderen Empfangsordner für jede definierte Nachrichtenklasse angeben oder angeben, dass eingehende Nachrichten für mehrere Nachrichtenklassen alle in denselben Ordner wechseln. Beispielsweise kann ein Client eine eigene Klasse von Nachrichten in einem eigenen Ordner eintreffen lassen. Eine Faxanwendung kann einen Ordner festlegen, in dem der Speicheranbieter eingehende Faxnachrichten und einen anderen Ordner, in dem der Anbieter ausgehende Faxe ablagert, ablagert.
  
Wenn beim Aufruf von **SetReceiveFolder** ein Fehler auftritt, bleibt die Einstellung des Empfangsordners unverändert. 
  
Wenn **SetReceiveFolder** die Einstellung des Empfangsordners mit  _lpEntryID_ auf NULL ändert und angibt, dass der Standard-Empfangsordner festgelegt werden soll, gibt **SetReceiveFolder** S_OK zurück, auch wenn keine Einstellung für die angegebene Nachrichtenklasse vorhanden war. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnSetReceiveFolder  <br/> |MFCMAPI verwendet die **IMsgStore::SetReceiveFolder-Methode,** um einen Ordner als Empfangsordner für eine bestimmte Nachrichtenklasse zu festlegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

