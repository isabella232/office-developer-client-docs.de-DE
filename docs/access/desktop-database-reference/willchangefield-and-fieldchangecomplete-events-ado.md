---
title: WillChangeField- und FieldChangeComplete-Ereignisse (ADO)
TOCTitle: WillChangeField and FieldChangeComplete Events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 40e9572988ca3335ef93ecf46d00a716ba29c595
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474837"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a>WillChangeField- und FieldChangeComplete-Ereignisse (ADO)


**Betrifft**: Access 2013 | Office 2013

Das **WillChangeField** -Ereignis wird aufgerufen, bevor der Wert eines oder mehrerer [Field](field-object-ado.md)-Objekte im [Recordset](recordset-object-ado.md)-Objekt durch einen ausstehenden Vorgang geändert wird. Das **FieldChangeComplete** -Ereignis wird aufgerufen, nachdem der Wert eines oder mehrerer **Field** -Objekte geändert wurde.

## <a name="syntax"></a>Syntax

WillChangeField-*cFields*, *Felder*, *AdStatus*, *pCommand*

FieldChangeComplete*cFields*, *Felder*, *pError*, *AdStatus*, *pCommand*

## <a name="parameters"></a>Parameter

  - *cFields*

  - Ein **Long**-Wert, der die Anzahl der **Field**-Objekte von *Fields* angibt.

  - *Fields*

  - Für **WillChangeField**ist der Parameter *Felder* Arrays von **Varianten** , die mit den ursprünglichen Werten **Field** -Objekte enthält.  
      
    Für **FieldChangeComplete**ist der Parameter *Felder* Arrays von **Varianten** , die mit den geänderten Werten **Field** -Objekte enthält.

  - *pError*

  - Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Wird **WillChangeField** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann.
    
    Wird **FieldChangeComplete** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Er wird auf **adStatusErrorsOccurred** festgelegt, wenn der Vorgang fehlgeschlagen ist.
    
    Legen Sie diesen Parameter vor der Rückgabe von **WillChangeField** auf **AdStatusCancel** fest, um den Abbruch des ausstehenden Vorgangs anzufordern.
    
    Legen Sie diesen Parameter vor der Rückgabe von **FieldChangeComplete** auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.

  - *pCommand*

  - Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.

## <a name="remarks"></a>Hinweise

Ein **WillChangeField** - oder ein **FieldChangeComplete** -Ereignis kann eintreten, wenn die [Value](value-property-ado.md)-Eigenschaft festgelegt und die [Update](update-method-ado.md)-Methode mit Feld- und Wertarrayparametern aufgerufen wird.

