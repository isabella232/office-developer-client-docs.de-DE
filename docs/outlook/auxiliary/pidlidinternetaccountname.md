---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: Gibt den Anzeigenamen des Kontos, das die Nachricht nicht übermittelt.
ms.openlocfilehash: 223bc5bbd485426676376d94875274613ff59685
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791185"
---
# <a name="pidlidinternetaccountname"></a><span data-ttu-id="aee06-103">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="aee06-103">PidLidInternetAccountName</span></span>

<span data-ttu-id="aee06-104">Gibt den Anzeigenamen des Kontos, das die Nachricht nicht übermittelt.</span><span class="sxs-lookup"><span data-stu-id="aee06-104">Returns the display name of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="aee06-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="aee06-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aee06-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="aee06-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aee06-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="aee06-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="aee06-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="aee06-108">Property set:</span></span>  <br/> |<span data-ttu-id="aee06-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="aee06-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="aee06-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="aee06-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="aee06-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="aee06-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="aee06-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="aee06-112">Data type:</span></span>  <br/> |<span data-ttu-id="aee06-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aee06-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="aee06-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="aee06-114">Area:</span></span>  <br/> |<span data-ttu-id="aee06-115">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="aee06-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aee06-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aee06-116">Remarks</span></span>

<span data-ttu-id="aee06-117">Diese Eigenschaft sollte den gleichen Wert enthalten, der von der Konto-Verwaltungs-API-Eigenschaft [PROP_ACCT_NAME](prop_acct_name.md) für das Konto zurückgegeben wird, die die Nachricht nicht übermittelt.</span><span class="sxs-lookup"><span data-stu-id="aee06-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_NAME](prop_acct_name.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="aee06-118">Nachricht-Anbieter Bereitstellen dieser benannten Eigenschaft und [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) , so dass folgende Aktionen ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="aee06-118">Message store providers expose this named property and [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="aee06-119">Wenn ein Benutzer **auf alle Antworten** in einer e-Mail-Nachricht klickt, entfernt Outlook die e-Mail-Adresse, die das Konto zugeordnet ist und für die Nachricht aus der Empfängerliste der Antwort versehen ist.</span><span class="sxs-lookup"><span data-stu-id="aee06-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="aee06-120">Dieses Verhalten tritt auf, es sei denn, diese e-Mail-Adresse der Absender der ursprünglichen Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="aee06-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="aee06-121">Standardmäßig wird Outlook sendet Antworten und weitergeleitete Nachrichten über das Konto auf die ursprüngliche Nachricht versehen ist.</span><span class="sxs-lookup"><span data-stu-id="aee06-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="aee06-122">In der Regel die Outlook-Protokollmanager Nachrichten übermittelt, und Outlook legt die Eigenschaften **PidLidInternetAccountName** und **PidLidInternetAccountStamp** , um das Konto anzugeben, das die Nachricht nicht übermittelt.</span><span class="sxs-lookup"><span data-stu-id="aee06-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="aee06-123">Wenn ein Nachrichtenspeichers eng mit einer Transport verknüpft ist, die Outlook-Protokollmanager übermittelt keine Nachrichten und Outlook diese Eigenschaften kann nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="aee06-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="aee06-124">In diesem Szenario ruft Outlook die [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="aee06-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="aee06-125">Wenn der Nachricht Speicheranbieter diese benannten Eigenschaften verfügbar zu machen möchte, muss **IMAPIProp::GetIDsFromNames** implementieren und Eigenschaftentags über die Ausgabe Parameter *LppPropTags* zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="aee06-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="aee06-126">Outlook kann mithilfe dieser Eigenschaftentags dann die [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) -Methode aufrufen, und der Nachricht Speicheranbieter den Kontonamen und Zeitstempel für das gewünschte Konto zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="aee06-126">Outlook can then call the [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="aee06-127">Zur Unterstützung der folgende benannten Eigenschaften erwarten Anbieter Outlook **IMAPIProp::GetIDsFromNames** verwendet, um das Eigenschafts-Tag für diese Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="aee06-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="aee06-128">Outlook gibt die folgenden Werte für die [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) -Struktur, die dieser benannten Eigenschaft entspricht, die als Teil des Arrays an, der input-Parameter *LppPropNames* des **IMAPIProp::GetIDsFromNames**auf zeigt übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="aee06-128">Outlook specifies the following values for the [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aee06-129">x LpGuid:</span><span class="sxs-lookup"><span data-stu-id="aee06-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="aee06-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="aee06-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="aee06-131">UlKind:</span><span class="sxs-lookup"><span data-stu-id="aee06-131">ulKind:</span></span>  <br/> |<span data-ttu-id="aee06-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="aee06-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="aee06-133">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="aee06-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="aee06-134">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="aee06-134">dispidInetAcctName</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aee06-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aee06-135">See also</span></span>

- [<span data-ttu-id="aee06-136">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="aee06-136">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="aee06-137">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="aee06-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="aee06-138">PidLidInternetAccountName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aee06-138">PidLidInternetAccountName Canonical Property</span></span>](http://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

