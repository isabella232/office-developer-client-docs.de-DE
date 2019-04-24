---
title: WillChangeField-und FieldChangeComplete-Ereignisse (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fd952cc09f410752f3eb7b5963059f8d6ee7c2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302485"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a><span data-ttu-id="3f267-102">WillChangeField-und FieldChangeComplete-Ereignisse (ADO)</span><span class="sxs-lookup"><span data-stu-id="3f267-102">WillChangeField and FieldChangeComplete events (ADO)</span></span>

<span data-ttu-id="3f267-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f267-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f267-p101">Das **WillChangeField** -Ereignis wird aufgerufen, bevor der Wert eines oder mehrerer [Field](field-object-ado.md)-Objekte im [Recordset](recordset-object-ado.md)-Objekt durch einen ausstehenden Vorgang geändert wird. Das **FieldChangeComplete** -Ereignis wird aufgerufen, nachdem der Wert eines oder mehrerer **Field** -Objekte geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3f267-p101">The **WillChangeField** event is called before a pending operation changes the value of one or more [Field](field-object-ado.md) objects in the [Recordset](recordset-object-ado.md). The **FieldChangeComplete** event is called after the value of one or more **Field** objects has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f267-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f267-106">Syntax</span></span>

<span data-ttu-id="3f267-107">WillChangeField*cFields*, *Fields*, *Status*, \*\* precordset</span><span class="sxs-lookup"><span data-stu-id="3f267-107">WillChangeField*cFields*, *Fields*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="3f267-108">FieldChangeComplete*cFields*, *Fields*, *pError*, instatus, \*\* precordset \*\*</span><span class="sxs-lookup"><span data-stu-id="3f267-108">FieldChangeComplete*cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="3f267-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f267-109">Parameters</span></span>

|<span data-ttu-id="3f267-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f267-110">Parameter</span></span>|<span data-ttu-id="3f267-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f267-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3f267-112">*cFields*</span><span class="sxs-lookup"><span data-stu-id="3f267-112">*cFields*</span></span> |<span data-ttu-id="3f267-113">Ein **Long**-Wert, der die Anzahl der **Field**-Objekte von *Fields* angibt.</span><span class="sxs-lookup"><span data-stu-id="3f267-113">A **Long** that indicates the number of **Field** objects in *Fields*.</span></span>|
|<span data-ttu-id="3f267-114">*Fields*</span><span class="sxs-lookup"><span data-stu-id="3f267-114">*Fields*</span></span> |<span data-ttu-id="3f267-115">Für **WillChangeField** ist der *Fields*-Parameter ein Array von **Variant**-Werten, die **Field**-Objekte mit den ursprünglichen Werten enthalten.</span><span class="sxs-lookup"><span data-stu-id="3f267-115">For **WillChangeField**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the original values.</span></span> <br/><br/><span data-ttu-id="3f267-116">
Für \*\*FieldChangeComplete*\* ist der \*Fields\*-Parameter ein Array von \*\*Variant\*\*-Werten, die \*\*Field\*\*-Objekte mit geänderten Werten enthalten.</span><span class="sxs-lookup"><span data-stu-id="3f267-116">For **FieldChangeComplete**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the changed values.</span></span>|
|<span data-ttu-id="3f267-117">*pError*</span><span class="sxs-lookup"><span data-stu-id="3f267-117">*pError*</span></span> |<span data-ttu-id="3f267-p102">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3f267-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="3f267-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="3f267-120">*adStatus*</span></span> |<span data-ttu-id="3f267-121">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="3f267-121">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="3f267-122">Wird **WillChangeField** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="3f267-122">When **WillChangeField** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="3f267-123">Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="3f267-123">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="3f267-124">Wird **FieldChangeComplete** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Er wird auf **adStatusErrorsOccurred** festgelegt, wenn der Vorgang fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="3f267-124">When **FieldChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="3f267-125">Legen Sie diesen Parameter vor der Rückgabe von **WillChangeField** auf **AdStatusCancel** fest, um den Abbruch des ausstehenden Vorgangs anzufordern.</span><span class="sxs-lookup"><span data-stu-id="3f267-125">Before **WillChangeField** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="3f267-126">Legen Sie diesen Parameter vor der Rückgabe von **FieldChangeComplete** auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="3f267-126">Before **FieldChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="3f267-127">*precordset*</span><span class="sxs-lookup"><span data-stu-id="3f267-127">*pRecordset*</span></span> |<span data-ttu-id="3f267-p104">Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3f267-p104">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3f267-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f267-130">Remarks</span></span>

<span data-ttu-id="3f267-131">Ein **WillChangeField**- oder ein **FieldChangeComplete**-Ereignis kann eintreten, wenn die [Value](value-property-ado.md)-Eigenschaft festgelegt und die [Update](update-method-ado.md)-Methode mit Feld- und Wertarrayparametern aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3f267-131">A **WillChangeField** or **FieldChangeComplete** event may occur when setting the [Value](value-property-ado.md) property and calling the [Update](update-method-ado.md) method with field and value array parameters.</span></span>

