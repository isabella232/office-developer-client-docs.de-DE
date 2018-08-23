---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 076fb4946af9a80e53fb8452d720c22b351f5ef6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572522"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ändert Attribute der Eigenschaften für ein [IMessage](imessageimapiprop.md) -Objekt, das von der Funktion [OpenIMsgOnIStg](openimsgonistg.md) bereitgestellt wird, oder legt diesen fest an. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Nachricht speichern-Anbieter  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a>Parameter

 _lpObject_
  
> [in] Zeiger auf das Objekt, für welche, das Eigenschaft Attribute festgelegt werden. 
    
 _lpPropTags_
  
> [in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die mit einem Array von Eigenschaftentags, der angibt, der Eigenschaften für die Eigenschaft Attribute festgelegt werden. 
    
 _lpPropAttrs_
  
> [in] Zeiger auf eine [SPropAttrArray](spropattrarray.md) -Struktur mit den Eigenschaftsattributen festlegen. 
    
 _lppPropProblems_
  
> [out] Zeiger auf das zurückgegebene [SPropProblemArray](spropproblemarray.md) -Struktur mit einem Satz von Eigenschaft Probleme. Diese Struktur identifiziert Probleme, wenn **SetAttribIMsgOnIStg** einige Eigenschaften festlegen können, jedoch nicht alle wurde. Wenn ein Zeiger auf NULL in der _LppPropProblems_ -Parameter übergeben wird, wird kein Problem Array-Eigenschaft zurückgegeben, selbst wenn einige Eigenschaften nicht festgelegt wurden. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber eine oder mehrere Eigenschaften konnte nicht zugegriffen werden und mit der Eigenschaftentyp PT_ERROR zurückgegeben wurden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eigenschaftsattribute nur auf Property-Objekte, d. h., durch Implementieren Objekte zugegriffen werden können die [IMAPIProp: IUnknown](imapipropiunknown.md) Schnittstelle. MAPI-Eigenschaften für ein OLE-Objekt strukturierter Speicher zur Verfügung zu stellen, [OpenIMsgOnIStg](openimsgonistg.md) erstellt eine [IMessage: IMAPIProp](imessageimapiprop.md) Objekt auf der Basis der OLE- **IStorage** -Objekt. Die Eigenschaftenattribute für solche Objekte können festgelegt oder mit **SetAttribIMsgOnIStg** geändert und mit [GetAttribIMsgOnIStg](getattribimsgonistg.md)abgerufen werden. 
  
 **Hinweis** **GetAttribIMsgOnIStg** und **SetAttribIMsgOnIStg** nicht für alle Objekte, die **IMessage** eingesetzt werden. Sie sind nur für **IMessage**- auf - von **OpenIMsgOnIStg**zurückgegebene **IStorage** Objekte gültig. 
  
In den _LpPropAttrs_ -Parameter müssen der Anzahl und die Position der Attribute der Anzahl und die Position der Eigenschaftentags im _LpPropTags_ -Parameter übergeben übereinstimmen. 
  
Die **SetAttribIMsgOnIStg** -Funktion wird verwendet, um Nachrichteneigenschaften schreibgeschützt, wenn das Schema **IMessage** erforderlich zu machen. Der Nachricht Store Beispielanbieter verwendet sie für diesen Zweck. Weitere Informationen finden Sie unter [Nachrichten](mapi-messages.md). 
  

