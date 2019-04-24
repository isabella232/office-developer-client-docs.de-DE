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
ms.openlocfilehash: efa5d60098fd5f16328669249a8445a124d9878b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317339"
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
  
> in Ein Zeiger auf die Nachrichtenklasse, die dem neuen Empfänger Ordner zugeordnet werden soll. Wenn der Parameter _lpszMessageClass_ auf NULL oder eine leere Zeichenfolge festgelegt ist, legt **SetReceiveFolder** den standardmäßigen Empfangsordner für den Nachrichtenspeicher fest. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Texttyp in den übergebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolge der Nachrichtenklasse ist im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Zeichenfolge der Nachrichtenklasse im ANSI-Format.
    
 _cbEntryID_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des Ordners, der als Empfänger Ordner eingerichtet werden soll. Wenn der Parameter _lpEntryID_ auf NULL festgelegt ist, ersetzt **SetReceiveFolder** den aktuellen Empfänger Ordner durch den Standardwert des Nachrichtenspeichers. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Ein Empfangsordner wurde erfolgreich eingerichtet.
    
## <a name="remarks"></a>Bemerkungen

Mit der **IMsgStore:: SetReceiveFolder** -Methode wird der Empfangsordner für eine bestimmte Nachrichtenklasse festgelegt oder geändert. Mit **SetReceiveFolder**kann ein Client mithilfe aufeinanderfolgender Aufrufe einen anderen Empfangsordner für jede definierte Nachrichtenklasse angeben oder angeben, dass eingehende Nachrichten für mehrere Nachrichtenklassen in denselben Ordner gelangen. Beispielsweise kann ein Client eine eigene Klasse von Nachrichten in seinem eigenen Ordner eingehen lassen. Eine Fax-Anwendung kann einen Ordner festlegen, in dem der Informationsspeicher Anbieter eingehende Faxe eingibt, und einen anderen Ordner, in dem der Anbieter ausgehende Faxe platziert.
  
Wenn während des Anrufs an **SetReceiveFolder**ein Fehler auftritt, bleibt die Einstellung für den Empfangsordner unverändert. 
  
Wenn **SetReceiveFolder** die Einstellung für den Empfänger Ordner mit _lpEntryID_ auf NULL festgelegt ändert, was darauf hinweist, dass der standardmäßige Empfangsordner festgelegt werden soll, gibt **SetReceiveFolder** S_OK zurück, auch wenn keine Einstellung für die angegebene Nachrichtenklasse. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnSetReceiveFolder  <br/> |MFCMAPI verwendet die **IMsgStore:: SetReceiveFolder** -Methode, um einen Ordner als Empfangsordner für eine bestimmte Nachrichtenklasse festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

