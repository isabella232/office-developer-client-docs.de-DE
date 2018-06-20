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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: edabb9a0f55cb34b4e144672e91ea50b8e9193b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792851"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**Betrifft**: Outlook 
  
Codiert eine Ansicht für die Empfänger einer Nachricht-Tabelle in der Datenstrom Transport-Neutral Encapsulation Format (TNEF) für die Nachricht an.
  
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
  
> [in] Ein Zeiger auf die Empfänger Tabelle, für die die Ansicht codiert ist. Der Parameter _LpRecipientTable_ kann NULL sein. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Transport-Anbieter, Nachricht-Anbieter und Gateways Aufruf der **ITnef::EncodeRecips** -Methode zum Ausführen von TNEF-Codierung für eine bestimmte Empfänger Tabelle-Ansicht. TNEF-Codierung ist nützlich, beispielsweise wenn für einen Anbieter oder ein Gateway einer bestimmten Spalte festlegen, die Sortierreihenfolge oder die Einschränkung für die Empfänger Tabelle erforderlich sind. 
  
Einen Anbieter oder Gateway übergibt die Tabellenansicht im Parameter _LpRecipientTable_ codiert werden. Die TNEF-Implementierung codiert Empfänger Tabelle, indem Sie die angegebene Ansicht, mit der angegebenen Spalte festlegen, Sortierreihenfolge, Einschränkung und Position. Wenn Sie einen Anbieter oder Gateway NULL _LpRecipientTable_übergibt, TNEF Ruft die Empfänger Tabelle aus der Nachricht mit der [IMessage::GetRecipientTable](imessage-getrecipienttable.md) -Methode codiert und verarbeitet jede Zeile der Tabelle in die TNEF-Stream mithilfe der Tabelle des aktuellen Einstellungen. 
  
Aufrufen von **EncodeRecips** mit NULL in _LpRecipientTable_ daher codiert alle Empfänger der Nachricht und entspricht dem Aufrufen der [ITnef::AddProps](itnef-addprops.md) -Methode mit dem TNEF_PROP_INCLUDE-Flag in seiner _UlFlags_ -Parameter und der **PR_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft im Parameter _LpPropList_ . 
  
Beachten Sie, dass es nur selten **EncodeRecips** aufrufen, es sei denn, es eine Voraussetzung zum Codieren von einer bestimmten Empfänger Tabellenansicht ist erforderlich ist. Fremde Messagingsysteme haben fast immer Funktionen für die Verarbeitung der Empfängerlisten, die leistungsstark genug, um den allgemeinen Anforderungen Codierung Empfängerlisten zu behandeln sind. Diese Systeme erfordern deshalb fast nie TNEF für diesen Zweck. 
  
## <a name="see-also"></a>Siehe auch



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[Kanonische PidTagMessageRecipients-Eigenschaft](pidtagmessagerecipients-canonical-property.md)
  
[ITnef: IUnknown](itnefiunknown.md)

