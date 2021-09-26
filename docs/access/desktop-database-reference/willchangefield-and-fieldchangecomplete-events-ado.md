---
title: WillChangeField- und FieldChangeComplete-Ereignisse (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a417141da9a213fc44bae95b93ce24887310d82e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621535"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a>WillChangeField- und FieldChangeComplete-Ereignisse (ADO)

**Gilt für**: Access 2013, Office 2013

Das **WillChangeField** -Ereignis wird aufgerufen, bevor der Wert eines oder mehrerer [Field](field-object-ado.md)-Objekte im [Recordset](recordset-object-ado.md)-Objekt durch einen ausstehenden Vorgang geändert wird. Das **FieldChangeComplete** -Ereignis wird aufgerufen, nachdem der Wert eines oder mehrerer **Field** -Objekte geändert wurde.

## <a name="syntax"></a>Syntax

WillChangeField *cFields*, *Fields*, *adStatus*, *pRecordset*

FieldChangeComplete *cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*cFields* |Ein **Long**-Wert, der die Anzahl der **Field**-Objekte von *Fields* angibt.|
|*Fields* |Für **WillChangeField** ist der *Fields*-Parameter ein Array von **Variant**-Werten, die **Field**-Objekte mit den ursprünglichen Werten enthalten. <br/><br/>
Für **FieldChangeComplete** ist der *Fields*-Parameter ein Array von **Variant**-Werten, die **Field**-Objekte mit geänderten Werten enthalten.|
|*Perror* |Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Wird **WillChangeField** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann. <br/><br/>Wird **FieldChangeComplete** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Er wird auf **adStatusErrorsOccurred** festgelegt, wenn der Vorgang fehlgeschlagen ist. <br/><br/>Legen Sie diesen Parameter vor der Rückgabe von **WillChangeField** auf **AdStatusCancel** fest, um den Abbruch des ausstehenden Vorgangs anzufordern. <br/><br/>Legen Sie diesen Parameter vor der Rückgabe von **FieldChangeComplete** auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.|
|*pRecordset* |Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.|

## <a name="remarks"></a>Bemerkungen

Ein **WillChangeField**- oder ein **FieldChangeComplete**-Ereignis kann eintreten, wenn die [Value](value-property-ado.md)-Eigenschaft festgelegt und die [Update](update-method-ado.md)-Methode mit Feld- und Wertarrayparametern aufgerufen wird.

