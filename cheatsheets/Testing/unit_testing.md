# Unit Testing (Vitest/Jest)

## Basic Matchers
- `expect(x).toBe(y)`: Precise equality.
- `expect(x).toEqual(y)`: Deep equality (objects/arrays).
- `expect(x).toBeNull()`
- `expect(x).toBeDefined()`
- `expect(x).toBeTruthy()` / `expect(x).toBeFalsy()`
- `expect(x).toContain(y)`: Array or string containment.
- `expect(x).toThrow()`: Check if function throws.

## Async Testing
```javascript
test('data is fetched', async () => {
  const data = await fetchData();
  expect(data).toBe('success');
});
```

## Mocks & Spies
- `vi.fn()` / `jest.fn()`: Create a mock function.
- `vi.spyOn(object, method)`: Spy on an existing method.
- `mockReturnValue(val)`
- `mockResolvedValue(val)`

## Hooks
- `beforeAll(() => { ... })`
- `beforeEach(() => { ... })`
- `afterEach(() => { ... })`
- `afterAll(() => { ... })`
