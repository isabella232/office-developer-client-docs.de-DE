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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 16e85eabc067bd82f5fb89c917afaf2831c75673
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439996"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft Attribute von Eigenschaften für ein [IMessage](imessageimapiprop.md) -Objekt ab, das von der [OpenIMsgOnIStg](openimsgonistg.md) -Funktion bereitgestellt wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Nachrichtenspeicher Anbieter  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>Parameter

 _lpObject_
  
> in Zeiger auf ein **IMessage** -Objekt, das von der [OpenIMsgOnIStg](openimsgonistg.md) -Funktion abgerufen wurde. 
    
 _lpPropTagArray_
  
> in Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags enthält, die die Eigenschaften angeben, für die Attribute abgerufen werden sollen. 
    
 _lppPropAttrArray_
  
> Out Zeiger auf einen Zeiger auf die zurückgegebene [SPropAttrArray](spropattrarray.md) -Struktur, die die abgerufenen Eigenschaftsattribute enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber auf eine oder mehrere Eigenschaften konnte nicht zugegriffen werden, und es wurde ein Eigenschaftentyp von PT_ERROR zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Auf Eigenschaftsattribute kann nur über Property-Objekte zugegriffen werden, also auf Objekte, die die [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle implementieren. Um MAPI-Eigenschaften für ein OLE Structured Storage-Objekt verfügbar zu machen, erstellt [OpenIMsgOnIStg](openimsgonistg.md) ein [IMessage: IMAPIProp](imessageimapiprop.md) -Objekt über dem OLE- **IStorage** -Objekt. Die Eigenschaftsattribute für solche Objekte können mit [SetAttribIMsgOnIStg](setattribimsgonistg.md) festgelegt oder geändert und mit **GetAttribIMsgOnIStg**abgerufen werden. 
  
> [!NOTE]
> **GetAttribIMsgOnIStg** und **SetAttribIMsgOnIStg** funktionieren nicht für alle **IMessage** -Objekte. Sie sind nur für **IMessage**-on- **IStorage** -Objekte gültig, die von **OpenIMsgOnIStg**zurückgegeben werden. 
  
Die Anzahl und Position der Attribute im _lppPropAttrArray_ -Parameter entsprechen der Anzahl und Position der Property-Tags im _lpPropTagArray_ -Parameter. 
  

