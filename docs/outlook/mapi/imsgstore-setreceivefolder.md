---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3745b8c9b779f40e9356efeec35a78025193965c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630516"
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
  
> [in] Ein Zeiger auf die Nachrichtenklasse, die dem neuen Empfangsordner zugeordnet werden soll. Wenn der  _Parameter lpszMessageClass_ auf NULL oder eine leere Zeichenfolge festgelegt ist, legt **SetReceiveFolder** den Standard-Empfangsordner für den Nachrichtenspeicher fest. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Texttyp in den übergebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolge der Nachrichtenklasse hat das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, hat die Nachrichtenklassenzeichenfolge das ANSI-Format.
    
 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Ordners, der als Empfangsordner eingerichtet werden soll. Wenn der  _Parameter lpEntryID_ auf NULL festgelegt ist, ersetzt **SetReceiveFolder** den aktuellen Empfangsordner durch den Standardwert des Nachrichtenspeichers. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Ein Empfangsordner wurde erfolgreich eingerichtet.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore::SetReceiveFolder-Methode** legt den Empfangsordner für eine bestimmte Nachrichtenklasse fest oder ändert diesen. Mit **SetReceiveFolder** kann ein Client mithilfe aufeinander folgender Aufrufe einen anderen Empfangsordner für jede definierte Nachrichtenklasse angeben oder angeben, dass eingehende Nachrichten für mehrere Nachrichtenklassen alle in denselben Ordner gehen. Beispielsweise kann ein Client eine eigene Klasse von Nachrichten in seinem eigenen Ordner empfangen lassen. Eine Faxanwendung kann einen Ordner festlegen, in dem der Speicheranbieter eingehende Faxe platziert, und einen anderen Ordner, in dem der Anbieter ausgehende Faxe ablegt.
  
Wenn während des Aufrufs von **SetReceiveFolder** ein Fehler auftritt, bleibt die Einstellung des Empfangsordners unverändert. 
  
Wenn **SetReceiveFolder** die Einstellung des Empfangsordners mit  _lpEntryID_ auf NULL ändert und angibt, dass der Standardempfängerordner festgelegt werden soll, gibt **SetReceiveFolder** S_OK zurück, auch wenn keine Einstellung für die angegebene Nachrichtenklasse vorhanden war. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnSetReceiveFolder  <br/> |MFCMAPI verwendet die **IMsgStore::SetReceiveFolder-Methode,** um einen Ordner als Empfangsordner für eine bestimmte Nachrichtenklasse festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

