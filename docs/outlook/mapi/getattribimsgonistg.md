---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ddb6d692a8e76a9c24affc3af9f612a6f1c0d769
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791778"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**Betrifft**: Outlook 
  
Ruft Attribute der Eigenschaften für ein [IMessage](imessageimapiprop.md) -Objekt, das von der Funktion [OpenIMsgOnIStg](openimsgonistg.md) bereitgestellt wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Nachricht speichern-Anbieter  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>Parameter

 _lpObject_
  
> [in] Zeiger auf ein **IMessage** -Objekt, das von der Funktion [OpenIMsgOnIStg](openimsgonistg.md) abgerufen. 
    
 _lpPropTagArray_
  
> [in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags enthält, der angibt, der Eigenschaften für die Attribute sind abgerufen werden sollen. 
    
 _lppPropAttrArray_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene [SPropAttrArray](spropattrarray.md) -Struktur, die abgerufene Eigenschaftenattribute enthält. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber eine oder mehrere Eigenschaften konnte nicht zugegriffen werden und mit der Eigenschaftentyp PT_ERROR zurückgegeben wurden.
    
## <a name="remarks"></a>Bemerkungen

Eigenschaftsattribute nur auf Property-Objekte, d. h., durch Implementieren Objekte zugegriffen werden können die [IMAPIProp: IUnknown](imapipropiunknown.md) Schnittstelle. MAPI-Eigenschaften für ein OLE-Objekt strukturierter Speicher zur Verfügung zu stellen, [OpenIMsgOnIStg](openimsgonistg.md) erstellt eine [IMessage: IMAPIProp](imessageimapiprop.md) Objekt auf der Basis der OLE- **IStorage** -Objekt. Die Eigenschaftenattribute für solche Objekte können festgelegt oder mit [SetAttribIMsgOnIStg](setattribimsgonistg.md) geändert und mit **GetAttribIMsgOnIStg**abgerufen werden. 
  
> [!NOTE]
> **GetAttribIMsgOnIStg** und **SetAttribIMsgOnIStg** nicht für alle Objekte, die **IMessage** eingesetzt werden. Sie sind nur für **IMessage**- auf - von **OpenIMsgOnIStg**zurückgegebene **IStorage** Objekte gültig. 
  
Die Anzahl und die Positionen der Attribute im _LppPropAttrArray_ -Parameter entsprechen der Anzahl und die Positionen der Eigenschaftentags im _LpPropTagArray_ -Parameter. 
  

