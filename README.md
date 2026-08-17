def rotate_right(items, positions):
    if not items:
        return []

    positions %= len(items)

    if positions == 0:
        return items.copy()

    return items[-positions:] + items[:-positions]


if __name__ == "__main__":
    values = ["A", "B", "C", "D", "E"]
    positions = 2

    print(f"Original: {values}")
    print(f"Rotated right: {rotate_right(values, positions)}")
