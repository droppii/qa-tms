# Gift PDP Test Suite

## Overview
Test suite for Gift PDP functionality including view, create, and search features.

## Test Cases

### View List Feature
1. [D4B-3009] Verify user will redirect to Gift list when click on Promotion/Gift
2. [D4B-3010] Verify Gift list has 6 fields
3. [D4B-3011] Verify user will redirect to Create Biz Gift when click on Create Biz Gift
4. [D4B-3012] Verify user will redirect to Create Mall Gift when click on Create Mall Gift
5. [D4B-3013] Verify system will show valid data if user input giftId in search box

### Create Gift Feature
1. [D4B-3020] Verify required fields validation
2. [D4B-3021] Verify gift creation for Business
3. [D4B-3022] Verify gift creation for Mall

## Test Data
```json
{
  "validGift": {
    "name": "Test Gift Card",
    "description": "Digital gift card for testing",
    "value": 100,
    "quantity": 50,
    "expiryDays": 30,
    "type": "DIGITAL"
  },
  "searchData": {
    "validGiftId": "GIFT-001",
    "invalidGiftId": "INVALID-001"
  }
}
```

## Prerequisites
- User must be logged in with admin privileges
- Test data must be prepared in the database

## Environment
- Testing Environment: Staging
- Browser Requirements: Chrome (latest), Firefox (latest)
- Mobile Responsiveness: Required

## Related Documentation
- [Navigation Steps](../shared-steps/navigation.md)
- [API Documentation](https://api-docs.example.com/gift-management)
