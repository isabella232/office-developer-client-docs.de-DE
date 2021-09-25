---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 39b3ee4328d63c45a822520a999ef2e429acecaf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592235"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Codiert eine Ansicht für die Empfängertabelle einer Nachricht im Transport-Neutral TNEF-Datenstrom (Encapsulation Format) für die Nachricht.
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpRecipientTable_
  
> [in] Ein Zeiger auf die Empfängertabelle, für die die Ansicht codiert ist. Der  _parameter lpRecipientTable_ kann NULL sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::EncodeRecips-Methode** auf, um die TNEF-Codierung für eine bestimmte Empfängertabellenansicht auszuführen. Die TNEF-Codierung ist beispielsweise nützlich, wenn ein Anbieter oder Gateway einen bestimmten Spaltensatz, eine bestimmte Sortierreihenfolge oder Einschränkung für die Empfängertabelle erfordert. 
  
Ein Anbieter oder Gateway übergibt die Tabellenansicht, die im  _lpRecipientTable-Parameter_ codiert werden soll. Die TNEF-Implementierung codiert die Empfängertabelle mit der angegebenen Ansicht unter Verwendung des angegebenen Spaltensatzes, der Sortierreihenfolge, der Einschränkung und der Position. Wenn ein Anbieter oder Gateway NULL in  _lpRecipientTable_ übergibt, ruft TNEF die Empfängertabelle aus der Nachricht ab, die mithilfe der [IMessage::GetRecipientTable-Methode](imessage-getrecipienttable.md) codiert wird, und verarbeitet jede Zeile der Tabelle mithilfe der aktuellen Einstellungen der Tabelle in den TNEF-Stream. 
  
Das Aufrufen von **EncodeRecips** mit NULL in _lpRecipientTable_ codiert somit alle Nachrichtenempfänger und entspricht dem Aufrufen der [ITnef::AddProps-Methode](itnef-addprops.md) mit dem flag TNEF_PROP_INCLUDE in seinem _ulFlags-Parameter_ und der **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) -Eigenschaft im _lpPropList-Parameter._ 
  
Beachten Sie, dass **EncodeRecips** nur selten aufgerufen werden muss, wenn eine bestimmte Empfängertabellenansicht codiert werden muss. Fremdnachrichtensysteme verfügen fast immer über Möglichkeiten für die Behandlung von Empfängerlisten, die leistungsfähig genug sind, um die allgemeinen Anforderungen der Codierung von Empfängerlisten zu erfüllen. daher benötigen diese Systeme für diesen Zweck fast nie TNEF. 
  
## <a name="see-also"></a>Siehe auch



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[PidTagMessageRecipients (kanonische Eigenschaft)](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

