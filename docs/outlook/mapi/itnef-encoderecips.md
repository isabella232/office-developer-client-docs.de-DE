---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d8caa503e557d35e259db743505d39ea4809dbfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348657"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Codiert eine Ansicht für die Empfängertabelle einer Nachricht im TNEF-Datenstrom (Transport-Neutral Encapsulation Format) für die Nachricht.
  
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
  
> in Ein Zeiger auf die Empfängertabelle, für die die Ansicht codiert ist. Der _lpRecipientTable_ -Parameter kann NULL sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Transport Anbieter, Nachrichtenspeicher Anbieter und Gateways rufen die **ITnef:: EncodeRecips** -Methode auf, um die TNEF-Codierung für eine bestimmte Empfänger Tabellenansicht durchzuführen. Die TNEF-Codierung ist beispielsweise nützlich, wenn ein Anbieter oder ein Gateway eine bestimmte Spaltengruppe, Sortierreihenfolge oder Einschränkung für die Empfängertabelle erfordert. 
  
Ein Anbieter oder Gateway übergibt die Tabellenansicht, die im Parameter _lpRecipientTable_ codiert werden soll. Die TNEF-Implementierung codiert die Empfängertabelle mit der angegebenen Ansicht, wobei der angegebene Spaltensatz, die Sortierreihenfolge, die Einschränkung und die Position verwendet werden. Wenn ein Anbieter oder ein Gateway in _LPRECIPIENTTABLE_NULL übergibt, ruft TNEF die Empfängertabelle aus der zu codierenden Nachricht mithilfe der [IMessage::](imessage-getrecipienttable.md) getrecipientable-Methode ab und verarbeitet jede Zeile der Tabelle im TNEF-Stream mithilfe der Aktuelle Einstellungen der Tabelle. 
  
Das Aufrufen von **EncodeRecips** mit NULL in _lpRecipientTable_ codiert daher alle Nachrichtenempfänger und entspricht dem Aufrufen der [ITnef::](itnef-addprops.md) AddProps-Methode mit dem TNEF_PROP_INCLUDE-Flag im _ulFlags_ -Parameter und dem **PR_ MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))-Eigenschaft im _lpPropList_ -Parameter. 
  
Beachten Sie, dass es selten erforderlich ist, **EncodeRecips** aufzurufen, es sei denn, eine bestimmte Empfänger Tabellenansicht muss codiert werden. Ausländische Messagingsysteme verfügen fast immer über Einrichtungen für die Verarbeitung von Empfängerlisten, die leistungsfähig genug sind, um die allgemeinen Anforderungen der Codierung von Empfängerlisten zu bewältigen. Daher benötigen diese Systeme für diesen Zweck fast nie TNEF. 
  
## <a name="see-also"></a>Siehe auch



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[Kanonische Pidtagmessagerecipients (-Eigenschaft](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

